<template>
  <div>
    <h1 class="font-500 main-title subtitulo mt-0">Graduação Presencial</h1>

    <v-layout
      class="flex-wrap align-center"
      :class="`flickity-mobile-${id}`"
      style="
        margin-left: calc(-8px - 0.4vw) !important;
        margin-right: calc(-8px - 0.4vw) !important;
      "
    >
      <v-flex
        xs12
        md6
        lg3
        class="spx-4 pb-4"
        v-for="({ name, slug, icon }, i) in cursos"
        :key="i"
      >
        <router-link
          class="no-underline"
          :to="`/faculdade-multiversa/graduacao-presencial/${slug}`"
        >
          <v-card>
            <v-img
              :src="$imagine('/blur-bg.jpg')"
              aspect-ratio="1.5"
              class="
                grey
                darken-4
                d-flex
                align-center
                justify-center
                text-center
              "
            >
              <h1 class="line-height-1">
                <i class="c-primary--text" :class="icon"></i>
              </h1>
              <h2 class="c-primary--text font-600">
                {{ name }}
              </h2>
            </v-img>
            <div class="c-primary" style="height: 5px"></div>
          </v-card>
        </router-link>
      </v-flex>
    </v-layout>
  </div>
</template>

<script>
import flick from '@/mixins/Flickity.js'

export default {
  mixins: [flick],

  data() {
    return {
      cursos: [
        {
          name: 'Direito',
          slug: 'direito',
          icon: 'fas fa-balance-scale',
        },
        {
          name: 'Administração',
          slug: 'administracao',
          icon: 'fas fa-briefcase',
        },
        {
          name: 'Pedagogia',
          slug: 'pedagogia',
          icon: 'fas fa-shapes',
        },
        {
          name: 'Psicologia',
          slug: 'psicologia',
          icon: 'fas fa-brain',
        },
      ],
    }
  },
}
</script>

