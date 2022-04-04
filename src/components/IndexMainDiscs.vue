<template>
  <main class="container px-5 mt-4 ">
    
        <div class="row flex-wrap row-cols-5 g-5 p-3">
            
              <MainListDisk 
                  v-for="(element,index) in filtradischi" :key="index"
                  :nome="element.author"
                  :genere="element.genre"
                  :poster="element.poster"
                  :titolo="element.title"
                  :anno="element.year"
                  class="col"
                />
          </div>
  </main>
</template>

<script>
import axios from"axios"
import MainListDisk from './MainListDisk.vue'
export default {
  name: 'IndexMainDiscs',
  components:{
    MainListDisk,
    
  },

  props : ['selezionaGeneri'],

  
data:function(){
        return{
          IndexMainDiscs: [],      
          generiList : [],      
        }
      },


  computed:{
    
    filtradischi(){
      if(this.selezionaGeneri === ''){
        console.log(this.selezionaGeneri)
        return this.generiList
        
      }
        return this.generiList.filter(
        (element) => element.genre === this.selezionaGeneri)
      
    }
  },

      
  created(){
    
      axios.get("https://flynn.boolean.careers/exercises/api/array/music")            //chiamata get
      .then((risultato)=>{                  // quando avrai una risposta il risultato dovrà comportare determinate cose
      
      console.log(risultato.data)
        this.generiList = risultato.data.response       // salvo i dischi nella variabile indexMain
        // lista generi
        this.generiList.forEach((element) => {
          if(!this.IndexMainDiscs.includes(element.genre)){
            this.IndexMainDiscs.push(element.genre)
          }
        });
        this.$emit('caricaGeneri', this.IndexMainDiscs)

      })
      .catch((errore) =>{                   // se non dovesse avveninire comunicheremo un determinato errore
        console.log(errore)
      })
    }
  }
  

</script>


<style scoped lang="scss">

</style> 
