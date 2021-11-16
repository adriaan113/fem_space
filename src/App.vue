<template>
  <div id="app">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <!-- <img :src="bg" alt=""> -->

    <!-- <h1>{{test}}</h1> -->
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld
  },
  data(){
    return {
      test: "nenenenene",
    }
    
  },
  computed:{
  },
}
</script>

<style lang="scss">

$medium:768px;
$large: 1440px;

*{
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  width: 100%;
  height: 100vh;

  background-image: url("./assets/home/background-home-mobile.jpg");
  background-size: cover;
  background-repeat: no-repeat;

  @media (min-width: $medium) {
     background-image: url("./assets/home/background-home-tablet.jpg");
  }

  @media (min-width: $large) {
     background-image: url("./assets/home/background-home-desktop.jpg");
  }
}

</style>
