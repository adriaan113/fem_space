<template>
    <nav>
        <v-app-bar flat app dark class="app-bar-color">
            <v-app-bar-title>
                <v-img :src="logo" height="50" contain class="mt-2"></v-img>
            </v-app-bar-title>
            <v-spacer></v-spacer>
            <v-app-bar-nav-icon class="mr-1" @click="drawer = !drawer"></v-app-bar-nav-icon>
        </v-app-bar>

        <v-navigation-drawer v-model="drawer" app right dark class="custom-drawer-style">
            <v-btn
            icon
            @click.stop="drawer = !drawer"
            class="satan mt-2 mb-4"
            >
                <v-icon>mdi-close</v-icon>
            </v-btn>
            <v-list>
            <!-- <v-list-item
                v-for="(item, i) in items"
                :key= "i"
                class="mb-3"
            >
                <v-list-item-title class="text-h6 font-weight-light text-uppercase">0{{i}} {{item.title}}</v-list-item-title>
            </v-list-item> -->
                <v-list-item>
                    <v-list-item-title>
                        <router-link to="/">00 HOME</router-link>
                    </v-list-item-title>
                </v-list-item>

                <v-list-item>
                    <v-list-item-title>
                        <router-link to="/destination">01 DESTINATION</router-link>
                    </v-list-item-title>
                </v-list-item>

                <v-list-item>
                    <v-list-item-title>
                        <router-link to="/crew">02 CREW</router-link>
                    </v-list-item-title>
                </v-list-item>

                <v-list-item>
                    <v-list-item-title>
                        <router-link to="/technology">03 TECHNOLOGY</router-link>
                    </v-list-item-title>
                </v-list-item>

            </v-list>
        </v-navigation-drawer>
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
.satan{
    margin-left: 85%;
}

.app-bar-color{
    background: transparent !important;
}

.custom-drawer-style{
    background: transparent !important;
    backdrop-filter: blur(15px);
    
}
</style>
