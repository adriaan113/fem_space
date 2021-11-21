<template>
    <section>
        <!-- menu -->
        <v-tabs centered dark v-model="tab" background-color="rgba(0,0,0,0)">
            <v-tab v-for="(planet, i) of planets" :key="i">{{planet.name}}</v-tab>
        </v-tabs>

        <v-tabs-items v-model="tab">
            <v-tab-item
            v-for="(planet,i) of planets"
            :key="i"
            >
                <v-card flat>
                    <v-img height="100" :src="require(`@/assets/destination/image-${planet.name.toLowerCase()}.webp`)"></v-img>
                    <v-card-title>{{planet.name}}</v-card-title>
                    <v-card-text v-text="planet.description"></v-card-text>
                </v-card>

                <!-- require('@/assets/destination/image-moon.webp') -->

            </v-tab-item>
        </v-tabs-items>

        <!-- <h1>{{planets[0].name}}</h1>
        <img :src="moon"> -->

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
      

        console.log(this.data);
        console.log(this.test);

        
    }
}
</script>

<style lang="scss">

</style>