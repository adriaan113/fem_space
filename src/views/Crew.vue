<template>
    <section>
        <v-carousel dark hide-delimiter-background :show-arrows="false" v-model="test" height="370" class="mt-10">
            <v-carousel-item
            v-for="(member,i) in crew"
            :key="i"
            :src="require(`@/assets/crew/image-${member.name.replace(/\ /g, '-').toLowerCase()}.webp`)"
            reverse-transition="fade-transition"
            transition="fade-transition"
            contain
            max-height="300"
            >
            </v-carousel-item>    
        </v-carousel>

        <v-card dark flat background-color="rgba(0,0,0,0)" v-model="test">

            <v-card-subtitle v-if="crew[test]" class="text-center text-uppercase pb-0">{{crew[test].role}}</v-card-subtitle>
            <v-card-title v-if="crew[test]" class="justify-center text-uppercase pt-1">{{crew[test].name}}</v-card-title>
            <v-card-text v-if="crew[test]" class="text-center mt-4 white--text pl-8 pr-8 body-1">{{crew[test].bio}}</v-card-text>
        </v-card>


    </section>    
</template>

<script>
import data from '../data'

export default {
    data(){
        return{
            crew: data.crew, 
            test:null,
        }
    },
     mounted(){
        const des= document.querySelector('.v-application--wrap');
        des.classList.add('crew'); 
        des.classList.remove('home', 'destination', 'technology');
        // console.log(this.crew[0].name.replace(/ /g, '-').toLowerCase());
        // console.log(this.crew[this.test].name);
    },
    
}
</script>

<style lang="scss" scoped>

.theme--dark.v-card{
    background: transparent !important;
}
    
</style>