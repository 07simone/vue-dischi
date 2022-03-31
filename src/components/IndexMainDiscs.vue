<template>
  <main >
    <div class="container">
        <div class="row">
      
      <div class="col-6 col-md-2 mx-3 my-2 " v-for="(element,index) in IndexMainDiscs" :key="index">
        <MainListDisk 
            :nome="element.author"
            :genere="element.genre"
            :poster="element.poster"
            :titolo="element.title"
            :anno="element.year"
          />
      </div>
  
    </div>
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
data:function(){
    return{
      IndexMainDiscs: null,
    }
  },
  created: function(){
    this.libraryApi();
  },

  methods:{
    libraryApi(){
      axios.get("https://flynn.boolean.careers/exercises/api/array/music")
      .then((risultato)=>{
        console.log(risultato.data)
        this.IndexMainDiscs = risultato.data.response
      })
      .catch((errore) =>{
        console.log(errore)
      })
    }
  }
  
}
</script>


<style scoped lang="scss">

main{
  background-color: rgb(12, 15, 39);
}
/* h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
} */
</style>
