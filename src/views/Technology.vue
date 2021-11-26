<template>
    <section>
        <v-carousel dark hide-delimiter-background :show-arrows="false"  delimiter-icon="mdi-checkbox-blank-circle" v-model="test">
            <v-carousel-item
            v-for="(kind,i) in tech"
            :key="i"
            :src="require(`@/assets/technology/image-${kind.name.replace(/\ /g, '-').toLowerCase()}-landscape.jpg`)"
            reverse-transition="fade-transition"
            transition="fade-transition"
            contain
            >
            </v-carousel-item>    
        </v-carousel>

        <v-card dark flat background-color="rgba(0,0,0,0)" v-model="test">
            <v-card-subtitle class="text-center text-uppercase"><div>the</div> <div>terminology</div></v-card-subtitle>
            <v-card-title v-if="tech[test]" class="justify-center text-uppercase pt-1">{{tech[test].name}}</v-card-title>
            <v-card-text v-if="tech[test]" class="text-center mt-4 white--text pl-8 pr-8 body-1">{{tech[test].description}}</v-card-text>
        </v-card>


    </section>    
</template>

<script>
import data from '../data'

export default {
    data(){
        return{
            tech: data.technology, 
            test:null,
        }
    },
     mounted(){
        const des= document.querySelector('.v-application--wrap');
        des.classList.add('technology'); 
        des.classList.remove('home', 'destination', 'crew');
    },
    
}
</script>

<style lang="scss" scoped>
.theme--dark.v-card{
    background: transparent !important;
}

.mdi-checkbox-blank-circle::before {
    content: "1" !important;
    opacity: 1 !important;
    color: red !important;
    z-index: 2 !important;
}

.v-icon.v-icon::after{
    opacity: 1 !important;
}

    
</style>