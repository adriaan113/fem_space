<template>
  <v-app>

     <v-app-bar dark>
        <v-img height="100%" contain position="left center" :src="logo"></v-img>
        <v-spacer></v-spacer>
        <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
        
        <!-- <v-toolbar-title>My files</v-toolbar-title> -->
  
       
  
      </v-app-bar>

      <v-navigation-drawer
        v-model="drawer"
        absolute
        right
        temporary
      >
        <v-list
          nav
        >
        <v-btn
            icon
            @click.stop="drawer = !drawer"
            right
            absolute
        >
          <v-icon>mdi-close</v-icon>
        </v-btn>

          <v-list-item-group
            v-model="group"
            active-class="deep-purple--text text--accent-4"
          >
            <v-list-item>
              <v-list-item-title>Foo</v-list-item-title>
            </v-list-item>
  
            <v-list-item>
              <v-list-item-title>Bar</v-list-item-title>
            </v-list-item>
  
            <v-list-item>
              <v-list-item-title>Fizz</v-list-item-title>
            </v-list-item>
  
            <v-list-item>
              <v-list-item-title>Buzz</v-list-item-title>
            </v-list-item>
          </v-list-item-group>
        </v-list>
      </v-navigation-drawer>


    <v-main>
      <router-view/>
    </v-main>

  </v-app>
</template>

<script>

export default {
  name: 'App',

  data: () => ({
    drawer: false,
    group: null,
    logo: require("./assets/space-logo.svg"),
  }),
  watch:{
    group () {
      this.drawer = false
    },
  }
};
</script>

<style lang="scss">


</style>
