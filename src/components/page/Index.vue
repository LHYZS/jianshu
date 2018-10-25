<template>
  <b-row>
    <b-col cols="9">
      <v-carousel></v-carousel>
      <v-menu></v-menu>
      <v-word></v-word>
    </b-col>
    <b-col cols="3">
      <v-tag></v-tag>
      <v-author></v-author>
    </b-col>
  </b-row>
</template>

<script>
  import vCarousel from '../common/Carousel';
  import vMenu from '../common/Menu';
  import vTag from '../common/Tag';
  import vWord from '../common/Word';
  import vAuthor from '../common/Author'

  export default {
    name: "Index",
    components: {
      vCarousel,
      vMenu,
      vTag,
      vWord,
      vAuthor,
    }
  }
</script>

<style scoped>

</style>
