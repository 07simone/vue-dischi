<template>
<nav class="navbar navbar-light bg-dark">
  <div class="container-fluid">
    <img class="img-fluid" src="https://cantabrialabsdifacooper.it/wp-content/uploads/2021/03/png-clipart-spotify-logo-spotify-computer-icons-podcast-music-apps-miscellaneous-angle-1-e1614848134495-300x300.png" alt="">
  <select v-model="selected">
    <option v-for="option in options" :value="option.value" :key=option>
      {{ option.text }}
    </option>
  </select>
  
  </div>
</nav>
</template>

<script>
export default {
  name: 'IndexHeader',


data:function(){
  return{
    selected: 'A',
      options: [
        { 
          text: 'Rock',
        },
        { 
          text: 'Pop',
        },
        { 
          text: 'Jazz',
        },
        { 
          text: 'Metal',
        },
      ]
  }
}
}


</script>


<style scoped lang="scss">

img{
  height: 80px;
}

</style>
