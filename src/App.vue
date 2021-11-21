<template>
  <v-app class="app-wrapper">

  <AppBarMobile class="d-flex d-sm-none"/>
  <AppBarDesktop class="d-none d-sm-flex"/>

    <v-main>
      <router-view/>
    </v-main>

  </v-app>
</template>

<script>

import AppBarMobile from '@/components/AppBarMobile'
import AppBarDesktop from '@/components/AppBarDesktop'

export default {
  name: 'App',
  components:{AppBarMobile,AppBarDesktop},
};
</script>

<style lang="scss">

.v-application--wrap{ //waarom deze selector en niet gewoon v-app?
  background-image: url("./assets/home/background-home-mobile.jpg");
  background-size: cover;
  @media(min-width: 600px){
    background-image: url("./assets/home/background-home-tablet.jpg");
  }
  @media(min-width: 960px){
    background-image: url("./assets/home/background-home-desktop.jpg");
  }
}

</style>
