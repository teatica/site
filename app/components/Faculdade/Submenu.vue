<template>
  <v-layout
    class="fill-width fixed"
    :class="passoudobanner ? 'elevation-2' : 'elevation-0'"
    style="z-index: 6; top: 64px; transition: all 0.3s"
    :style="{
      marginTop: onFooter ? '-100px' : '0',
    }"
  >
    <v-flex xs12 md4 lg2 :class="passoudobanner ? 'white' : 'transparent'">
    </v-flex>
    <v-flex
      xs12
      md8
      lg10
      class="text-right spr-24 submenu"
      :class="passoudobanner ? 'white' : 'mycolor'"
    >
      <v-btn
        depressed
        v-for="(item, i) in items"
        :key="i"
        :to="item.path"
        class="fill-height transparent spx-4 no-radius mx-0"
        :class="{
          'is-active': item.path === pathname,
          'white--text': !passoudobanner,
          'c-secondary--text': passoudobanner,
        }"
        >{{ item.name }}</v-btn
      >
    </v-flex>
  </v-layout>
</template>

<script>
export default {
  props: ['onFooter', 'isup', 'banner'],
  data() {
    return {
      passoudobanner: false,
      pathname: '',
      items: [
        { name: 'Início', path: '/faculdade-multiversa' },
        {
          name: 'Graduação Presencial',
          path: '/faculdade-multiversa/graduacao-presencial',
        },
        {
          name: 'Graduação Digital',
          path: '/faculdade-multiversa/graduacao-digital',
        },
        { name: 'Pós-Graduação', path: '/faculdade-multiversa/pos-graduacao' },
        {
          name: 'Turismo e Hotelaria',
          path: '/faculdade-multiversa/portal-de-turismo-e-hotelaria',
        },
        {
          name: 'Extensão Digital',
          path: '/faculdade-multiversa/extensao-digital',
        },
        { name: 'Metodologia', path: '/faculdade-multiversa/metodologia' },
      ],
    }
  },

  $route(to, from) {
    this.pathname = to.fullPath
  },
  mounted() {
    this.pathname = location.pathname
    this.$nextTick(() => {
      // let item = this.items.find((i) => i.name === 'Metodologia')
      // let path =
      //   location.pathname === '/faculdade-multiversa'
      //     ? '#metodologia'
      //     : '/faculdade-22#metodologia'
      // item.path = path
      setTimeout(() => {
        let bh = this.banner.$el.offsetHeight - 76 - 48
        this.passoudobanner = bh < scrollY
        addEventListener('scroll', () => {
          this.passoudobanner = bh < scrollY
        })
      }, 1000)
    })
  },
}
</script>

<style style="scss">
.mycolor {
  background: linear-gradient(
    to left,
    #1f294d,
    #1f294d,
    #1a2344,
    transparent,
    transparent
  );
}
.theme--light.v-btn--active::before {
  opacity: 0 !important;
}
.v-btn.is-active::before {
  opacity: 0.2 !important;
}
.submenu .v-btn.v-size--default {
  font-size: calc(10px + 0.2vw);
}
</style>