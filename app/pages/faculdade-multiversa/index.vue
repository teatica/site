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
    <Banner
      txt1="FACULDADE"
      txt2="MULTIVERSA"
      img="/banners/faculdade.jpg"
      ref="banner"
    ></Banner>
    <div class="spx-sm-24 spt-24 spx-xs-15">
      <PosCarousel
        :cursos="pos"
        titulo="Pós-graduação"
        tipo="pos-graduacao"
        doFlick
      ></PosCarousel>
      <FaculdadeCarouselPresencial></FaculdadeCarouselPresencial>
      <CarouselEmBreve titulo="Graduação Digital"></CarouselEmBreve>
    </div>

    <div class="spx-24">
      <h1 class="font-500 smt-20 main-title subtitulo">Extensão Digital</h1>
      <PosCarousel
        :cursos="cursos"
        tipo="extensao-digital"
        doFlick
      ></PosCarousel>
    </div>
    <br />
    <br />
    <br />
    <br />
  </div>
</template>

<script>
import cursos from '@/data/cursos-turismo.js'
import pos from '@/data/pos.js'

export default {
  data() {
    return {
      banner: {},
      cursos,
      pos,
    }
  },
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
    }, 500)
  },
}
</script>

<style lang="scss">
.submenu {
  .v-btn {
    font-size: 13px;
  }
}
</style>

