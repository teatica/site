<template>
  <v-card>
    <v-img
      :lazy-src="$imagine('/placeholder-2.jpg')"
      aspect-ratio="1.5"
      class="
        c-info-lighten-2
        d-flex
        align-center
        justify-center
        text-center
        c-info-darken-2--text
      "
    >
      <span class="spx-5" style="border: 1px solid #f9d428"
        >em breve</span
      ></v-img
    >
  </v-card>
</template>
<script>
export default {
  props: ['blog'],
}
</script>
<style lang='scss'>
</style>