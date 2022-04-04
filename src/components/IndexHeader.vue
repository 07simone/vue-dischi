<template>
<header>
  <nav class="navbar navbar-light bg-dark d-flex justify-content-between ">
      <div class="container-fluid">
          <div class="img">
              <img class="img-fluid" src="https://cantabrialabsdifacooper.it/wp-content/uploads/2021/03/png-clipart-spotify-logo-spotify-computer-icons-podcast-music-apps-miscellaneous-angle-1-e1614848134495-300x300.png" alt="">
          </div>
          <div class="">
              <select class="form-select" 
              v-model="selezionaGeneri" 
              @change="$emit('cambiaGenre', selezionaGeneri)"
              >
                <option value="">Open menu genres</option> 
                <option v-for="(element,index) in generiList" :key="index" :value="element">{{element}}</option>
              </select>
          </div>
      </div>
  </nav>
</header>

</template>

<script>
export default {
  name: 'IndexHeader',
  props: {generiList: Array},

  data:function(){
    return {
      selezionaGeneri : "",   // connetto questa variabile con il v-model con la select
    }
  },

methods:{
  
}
}




</script>


<style scoped lang="scss">

img{
  height: 80px;
}

</style>
