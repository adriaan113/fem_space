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
  methods:{
    // homeBg(){
    //     const home= document.querySelector('.v-application--wrap');
    //     home.classList.add('home');
    // },
    // destinationBg(){
    //   const des= document.querySelector('.v-application--wrap');
    //   des.classList.add('destination');
    // }

  },

  // mounted(){
  //   this.homeBg();
  //   this.destinationBg();
  // },  
};
</script>

<style lang="scss">

// @import './assets/global.scss';

.v-application--wrap{
  
  // height: 100vh;

  //waarom deze selector en niet gewoon v-app?
  // background-image: url("./assets/home/background-home-mobile.jpg");
  // background-size: cover;
  // @media(min-width: 600px){
  //   background-image: url("./assets/home/background-home-tablet.jpg");
  // }
  // @media(min-width: 960px){
  //   background-image: url("./assets/home/background-home-desktop.jpg");
  // }
}

</style>
