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

</style>
