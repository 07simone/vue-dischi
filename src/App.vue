<template>
  <div id="app">


  <IndexHeader/>


  <IndexMainDiscs/>
  
  </div>
</template>

<script>

import IndexHeader from './components/IndexHeader.vue'
import IndexMainDiscs from './components/IndexMainDiscs.vue'


export default {
  name: 'App',
  components: {
    IndexHeader,
    IndexMainDiscs
  },


}
</script>

<style lang="scss">
@import "@/style/main-style.scss";


#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
 /*  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px; */
}
</style>
