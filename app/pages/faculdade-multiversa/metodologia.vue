<template>
  <div id="metodologia">
    <FaculdadeSubmenu
      :isup="isup"
      :onFooter="onFooter"
      :banner="banner"
      class="hidden-md-and-down"
    ></FaculdadeSubmenu>
    <Banner
      img="/banners/metodologia.jpg"
      hasMobileImg
      hasTabletImg
      txt1="METODOLOGIA"
      txt2="EDUCACIONAL"
      ref="banner"
    ></Banner>
    <div
      class="spx-sm-24 spx-xs-15 grey lighten-3"
      style="padding-bottom: calc(45px + 3vw)"
    >
      <div class="ead-padding spb-10 spt-15">
        <v-layout wrap class="spt-2">
          <v-flex
            xs12
            md6
            v-for="({ title, desc, icon }, i) in diferenciais"
            :key="i"
            class="spr-15 spy-8"
          >
            <v-layout class="hover-effect-1 metodologia-wrap">
              <!-- <div
                class="
                  borda-diferenciais-icone
                  mr-5
                  d-flex
                  justify-center
                  align-center
                "
              >
                <i :class="`fas fa-${icon} c-primary--text`"></i>
              </div> -->
              <div class="borda-metodologia hover-effect-1-borda mx-0">
                <h1
                  class="
                    number
                    secondary--text
                    white
                    d-flex
                    align-center
                    justify-center
                  "
                  style="width: 90%; height: 90%; border-radius: 100px"
                >
                  <i :class="`fas fa-${icon} c-primary-darken-1--text`"></i>
                </h1>
              </div>
              <div class="ml-3">
                <p
                  class="
                    smb-1
                    titulo-fluxograma
                    c-secondary--text
                    font-600
                    text-uppercase
                  "
                >
                  <big>{{ title }}</big>
                </p>
                <p class="smb-0 c-info-darken-3--text">
                  {{ desc }}
                </p>
              </div>
            </v-layout>
          </v-flex>
        </v-layout>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  computed: {
    isup() {
      return this.$attrs.isup
    },
    onFooter() {
      return this.$attrs.onFooter
    },
  },
  mounted() {
    setTimeout(() => {
      this.banner = this.$refs.banner
    }, 900)
  },
  data() {
    return {
      banner: {},

      diferenciais: [
        {
          icon: 'plus',
          title: 'Máxima aplicabilidade',
          desc: 'A cada trilha o aluno aplica seu projeto à sua realidade profissional.',
        },
        {
          icon: 'comments',
          title: 'Momentos ao vivo de interação',
          desc: 'Momentos de orientação ao vivo com docentes especializados.',
        },
        {
          icon: 'id-card',
          title: 'Master Class com especialistas',
          desc: 'Master Class ao vivo com pessoas que são autoridades em inovação em educação',
        },
        {
          icon: 'chalkboard-teacher',
          title: 'Preceptoria',
          desc: 'Acompanhamento e feedback  personalizado com docentes experientes.',
        },
        {
          icon: 'user',
          title: 'Assessoramento individual',
          desc: 'Assessoria de tutor para organização e suporte técnico nos processos do curso.',
        },
        {
          icon: 'cubes',
          title: 'Nano degree (Certificados Parciais)',
          desc: 'Certificados de competências ao longo do curso, enriquecendo seu currículo antes mesmo de concluir  todo o MBA.',
        },
        {
          icon: 'cogs',
          title: 'Aprendizagem personalizada',
          desc: 'Todos os projetos aplicados durante o curso consideram as necessidades do contexto profissional do aluno.',
        },
      ],
    }
  },
}
</script>

<style lang="scss">
@import '@/../scss/_color_set';

.borda-diferenciais-icone {
  width: calc(60px + 1vw);
  min-width: calc(60px + 1vw) !important;
  background: rgb(0, 0, 0);
  border-radius: 1000px;
}
// .lapela-1 {
//   position: absolute;
//   left: -7px;
//   width: 0;
//   height: 0;
//   border-top: 18px solid transparent;
//   border-bottom: 0px solid transparent;
//   border-right: 7px solid #bfa400;
// }

.borda-metodologia {
  border-top: 3px solid #8a8a8a;
  border-bottom: 3px solid #8a8a8a;
  border-left: 1px solid #ffffff;
  border-right: 1px solid #ffffff;
  border-radius: 100%;
  margin: 0 auto;
  min-width: calc(60px + 1vw);
  width: calc(60px + 1vw);
  height: calc(60px + 1vw);
}

.metodologia-wrap {
  @media (min-width: 769px) {
    align-items: center;
  }
}
</style>
