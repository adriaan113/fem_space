<template>
    <nav>
        <v-app-bar flat app dark class="app-bar-color">
            <v-app-bar-title>
                <v-img :src="logo" height="50" contain class="mt-2"></v-img>
            </v-app-bar-title>
            <v-spacer></v-spacer>
            <v-tabs class="d-flex" right>
                <v-tab>
                    <router-link to="/">00 HOME</router-link>
                </v-tab>

                <v-tab>
                    <router-link to="/destination">01 DESTINATION</router-link>  
                </v-tab>

                <v-tab>
                    <router-link to="/crew">02 CREW</router-link>
                </v-tab>

                <v-tab>
                    <router-link to="/technology">03 TECHNOLOGY</router-link>
                </v-tab>
            </v-tabs>
        </v-app-bar>
    </nav>
</template>

<script>

export default {

    data: () => ({
    logo: require("../assets/space-logo.svg"),
    drawer: false,
    items: [
        { title: 'home' },
        { title: 'destination' },
        { title: 'crew' },
        { title: 'technology' },
      ],
  }),
}

</script>

<style lang="scss">
    // .v-toolbar__content{
    //     // padding-right: 0;
    // }

    .v-tabs{
        flex: 0 1 auto !important;
        width: auto !important; 
    }
</style>
