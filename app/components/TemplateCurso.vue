<template>
  <div class="white">
    <div slot="submenu" class="fill-with">
      <FaculdadeSubmenu
        :isup="isup"
        :onFooter="onFooter"
        :banner="banner"
        class="hidden-md-and-down"
      ></FaculdadeSubmenu>
    </div>
    <PosShowBanner
      :titulo="curso.name"
      :inscricao="curso.inscricao"
      :imagem="curso.img"
      :categoria="curso.categoria ? curso.categoria : 'Pós-graduação'"
      ref="banner"
    ></PosShowBanner>

    <PosShowSobreOCurso
      class="smx-sm-24 smx-xs-7 spx-xl-24"
      :inscricao="curso.inscricao"
      :titulo="curso.name"
      :descricao="curso.descricao"
      :duracao="curso.duracao"
      :slug="curso.slug"
      :inicio="setInicio"
      :carga_horaria="curso.carga_horaria"
      :investimento="decodedPrecos"
      :type="checkClass"
      :modalidade="curso.modalidade"
    ></PosShowSobreOCurso>
    <div style="clear: both"></div>

    <PosShowDiferenciaisCurso
      v-if="curso.diferenciais && curso.diferenciais.length"
      :diferenciais="curso.diferenciais"
    ></PosShowDiferenciaisCurso>
    <PosShowCompetencias
      :competencias="curso.competencias"
      :titulo="curso.name"
      :slug="curso.slug"
      class="smx-24 smx-xs-0"
      :check-class="checkClass"
    ></PosShowCompetencias>

    <div class="white relative" style="z-index: 1">
      <div class="smx-sm-24 smx-xs-0">
        <PosShowComponenteCurricular
          class="spx-xs-7 spx-xs-7 spx-lg-24"
          v-if="curso.matrizes && curso.matrizes.length"
          :matrizes="curso.matrizes"
          :carga-horaria="curso.carga_horaria"
        ></PosShowComponenteCurricular>
      </div>

      <PosShowEquipe
        :professores="curso.professores"
        v-if="curso.professores && curso.professores.length"
        class="spb-20"
      ></PosShowEquipe>

      <PosShowParceiros
        v-if="curso.parceiros && curso.parceiros.length"
        :parceiros="curso.parceiros"
      ></PosShowParceiros>

      <PosFluxograma
        v-if="tipo === 'pos-graduacao'"
        style="z-index: 3"
      ></PosFluxograma>
      <div></div>

      <PosShowBannerSaibaMais></PosShowBannerSaibaMais>

      <div class="spx-sm-24 spx-xs-15 spb-24">
        <PosCarousel
          titulo="Outros cursos"
          :cursos="cursos"
          doFlick
          :tipo="tipo"
        ></PosCarousel>
      </div>
      <br />
      <br />
      <br />
      <br />
    </div>
  </div>
</template>
<script>
export default {
  props: ['cursos', 'curso', 'check-class', 'isup', 'onFooter', 'tipo'],
  data() {
    return {
      banner: {},
    }
  },
  computed: {
    setInicio() {
      let inicio

      if (this.curso.turmas && this.curso.turmas.length) {
        let txt = (t, i) => {
          return (
            `<span class="font-600">Turma 0${i + 1}</span>: ` +
            t.inicio +
            (t.horario ? ' - ' + t.horario : '') +
            '<br>'
          )
        }
        this.curso.turmas.forEach((t, i) => {
          inicio = inicio ? inicio + txt(t, i) : txt(t, i)
        })
      } else {
        inicio = this.curso.data_inicio
          ? this.curso.data_inicio +
            ' de ' +
            this.curso.mes_inicio +
            ' de ' +
            this.curso.ano_inicio
          : '' + this.curso.mes_inicio + ' de ' + this.curso.ano_inicio
      }
      return inicio
    },

    decodedPrecos() {
      if (this.curso.investimento) {
        if (typeof this.curso.investimento === 'string') {
          return JSON.parse(this.curso.investimento)
        } else {
          return this.curso.investimento
        }
      } else {
        return []
      }
    },
  },
  mounted() {
    setTimeout(() => {
      this.banner = this.$refs.banner
    }, 500)
  },
}
</script>
<style lang='scss'>
</style>