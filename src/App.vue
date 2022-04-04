<template>
  <div id="app">


  <IndexHeader :generiList="generiList"  @cambiaGenre="aggiornaSelezionaGeneri"/>


  <IndexMainDiscs @caricaGeneri ="aggiornaGeneriList" :selezionaGeneri="selezionaGeneri"/>
  
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

  data: function(){
    return{
      generiList : [],
      selezionaGeneri:'', 
    }
  },
methods:{
  aggiornaGeneriList(generiList){
    this.generiList = generiList
  },
  aggiornaSelezionaGeneri(selezionaGeneri){
    this.selezionaGeneri = selezionaGeneri
  }
}

}
</script>

<style lang="scss">
@import "./style/main-style.scss";


</style>
