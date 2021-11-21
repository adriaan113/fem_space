<template>
  <!-- <hello-world /> -->
  <div class="home-wrapper d-flex flex-column align-center">

    <v-card dark max-width="500" class="mr-5 mb-10 ml-5 d-flex flex-column align-center card">
      <v-card-subtitle class="text-h6 font-weight-light text-center text-uppercase">so,you want to travel to</v-card-subtitle>
      <v-card-title class="text-h1 font-weight-light justify-center text-uppercase">space</v-card-title>
      <v-card-text class="text-body-1 text-center mt-8">Let’s face it; if you want to go to space, you might as well genuinely go to outer space and not hover kind of on the edge of it. Well sit back, and relax because we’ll give you a truly out of this world experience!</v-card-text>
    </v-card>

    <v-card light width="200" height="200" class="rounded-circle mx-auto d-flex flex-column align-center justify-center text-uppercase">
      <v-card-title class="justify-center">explore</v-card-title>
    </v-card>

  </div>
</template>

<script>
  // import HelloWorld from '../components/HelloWorld'

  export default {
    name: 'Home',

    components: {
      // HelloWorld,
    },
  }
</script>

<style lang="scss">

.home-wrapper{
  height: calc(100vh - 50px);
  .card{
    background: transparent !important;
  }
}
</style>
