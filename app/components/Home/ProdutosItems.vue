<template>
  <v-layout
    class="
      spx-20
      produtos-items-wrap
      flex-wrap
      justify-space-evenly
      white
      fill-height
      align-center
    "
  >
    <v-flex
      xs12
      sm6
      lg3
      v-for="({ nome, img, url }, i) in produtos"
      :key="i"
      data-aos="fade-right"
      :data-aos-delay="i * 100"
      class="smy-10"
    >
      <router-link
        :to="url"
        class="no-underline c-secondary--text produtos-items"
      >
        <v-img
          style="max-width: 100px"
          class="mx-auto produtos-items-img"
          contain
          :src="$imagine(img)"
        ></v-img>
        <h1 class="subtitulo2 font-900 text-center text-uppercase">
          {{ nome }}
        </h1>
      </router-link>
    </v-flex>
  </v-layout>
</template>

<script>
export default {
  data() {
    return {
      produtos: [
        {
          nome: 'Faculdade Multiversa',
          img: '/produtos/t-04.png',
          url: '/faculdade-multiversa',
        },
        {
          nome: 'Portal de Turismo e Hotelaria',
          img: '/produtos/t-01.png',
          url: '/faculdade-multiversa/portal-de-turismo-e-hotelaria',
        },
        {
          nome: 'Colégio Multiversa',
          img: '/produtos/t-03.png',
          url: '/colegio-multiversa',
        },
        {
          nome: 'Portal de Cursos Digitais',
          img: '/produtos/t-02.png',
          url: '/portal-de-cursos-digitais',
        },
        {
          nome: 'Escola de Saúde',
          img: '/produtos/t-06.png',
          url: '/escola-de-saude',
        },
        {
          nome: 'Centro Integrado de Saúde',
          img: 'produtos/t-05.png',
          url: '/centro-integrado-de-saude',
        },
        {
          nome: 'Hospital Veterinário',
          img: '/produtos/t-07.png',
          url: '/hospital-veterinario',
        },
        {
          nome: 'Hub de Inovação',
          img: '/produtos/t-08.png',
          url: '/hub-de-inovacao',
        },
        // {
        //   nome: 'Gestão Interina de IES',
        //   img: '/produtos/t-01.png',
        //   url: '/gestao-interina-de-ies',
        // },
      ],
    }
  },
}
</script>

<style lang="scss">
.produtos-items-wrap {
  padding: 50px;
  @media (min-height: 1600px) {
    margin-top: -50px;
    margin-bottom: -50px;
    padding-top: 50px !important;
  }
}
.produtos-items {
  .v-image {
    transition: all 0.3s;
  }
  &:hover {
    .v-image {
      transform: scale(1.08);
    }
  }
}
</style>