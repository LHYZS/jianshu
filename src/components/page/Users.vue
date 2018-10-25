<template>
  <b-row>
    <b-col cols="9">
      <v-personal></v-personal>
      <v-word></v-word>
    </b-col>
    <b-col>
      <v-introduce></v-introduce>
    </b-col>
  </b-row>
</template>

<script>
  import vWord from '../common/Word';
  import vPersonal from '../common/Personal';
  import vIntroduce from '../common/Introduce';

  export default {
    name: "Users",
    components: {
      vPersonal,
      vWord,
      vIntroduce,
    }
  }
</script>

<style scoped>

</style>
