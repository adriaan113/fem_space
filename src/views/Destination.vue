<template>
    <section class="d-flex flex-column align-center des-wrapper">
        <!-- menu -->
        <v-tabs centered dark v-model="tab" background-color="rgba(0,0,0,0)" class="mt-4">
            <v-tab v-for="(planet, i) of planets" :key="i">{{planet.name}}</v-tab>
        </v-tabs>

        <v-tabs-items v-model="tab">
            <v-tab-item
            v-for="(planet,i) of planets"
            :key="i"
            >
                <v-card dark flat background-color="rgba(0,0,0,0)" class="d-flex flex-column align-center">
                    <v-img max-width="200" contain class="planet-img mt-5" :src="require(`@/assets/destination/image-${planet.name.toLowerCase()}.webp`)"></v-img>
                    <v-card-title class="text-h2 font-weight-light text-uppercase">{{planet.name}}</v-card-title>
                    <v-card-text class="text-center" v-text="planet.description"></v-card-text>
                    <v-divider dark class="divider mt-3 mb-3"></v-divider>

                    <v-card-subtitle class="text-uppercase">avg. distance</v-card-subtitle>
                    <v-card-text class="text-h5 text-center white--text text-uppercase" v-text="planet.distance"></v-card-text>

                    <v-card-subtitle class="text-uppercase">est. travel time</v-card-subtitle>
                    <v-card-text class="text-h5 text-center white--text text-uppercase" v-text="planet.travel"></v-card-text>
                </v-card>
            </v-tab-item>
        </v-tabs-items>
    </section>
</template>

<script>
import data from '../data'

export default {
    data(){
        return{
            tab: null,
            data: data,
            planets: data.destinations,  
            planetImage: data.destinations[0].name.toLowerCase(),
        }
    },
    computed:{
     
    },
    methods:{
    },
    mounted(){
        const des= document.querySelector('.v-application--wrap');
        des.classList.add('destination'); 
        des.classList.remove('home');
    },
}
</script>

<style lang="scss">

@import '../assets/global.scss';

    .v-card{
        background: transparent !important;
    }

    .des-wrapper{
        height: calc(100vh - 50px);
    }


    .theme--light.v-tabs-items{
        background: transparent;
    }

    .theme--dark.v-divider{
        border-color: white !important;
        border-width: thin 0 0 0;
        width: 80%;
    }

    // .planet-img{
    //     position: absolute;
    //     top:0;
    //     left:0;
    // }
</style>