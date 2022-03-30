<template>
  <div id="app">


  <IndexHeader/>


  <IndexMain/>
  
  </div>
</template>

<script>
import axios from"axios"
import IndexHeader from './components/IndexHeader.vue'
import IndexMain from './components/IndexMainDiscs.vue'


export default {
  name: 'App',
  components: {
    IndexHeader,
    IndexMain
  },
  created: function(){
    this.libraryApi();
  },

  methods:{
    libraryApi(){
      axios.get("https://flynn.boolean.careers/exercises/api/array/music")
      .then((risultato)=>{
        console.table(risultato.data.response)
      })
      .catch((errore) =>{
        console.log(errore)
      })
    }
  }
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
