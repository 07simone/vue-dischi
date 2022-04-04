<template>
<div>
<div class="card p-3 text-center ">
        <img class="img-fluid mb-3"  :src="poster"  :alt="nome">
      
          <h5 class="card-title mb-0 fs-3">{{nome}}</h5> 
          <h3 class="card-title mb-0 fs-3">{{titolo}}</h3>
          <p class="card-text">{{genere}}</p>
          <p class="card-text">{{anno}}</p> 
      
</div>
</div>
    
</template>

<script>
export default {
  name: 'IndexMain',
  props:["nome","genere","poster","titolo","anno"]

}
</script>


<style  lang="scss">

div.card{
  font-size: 0.9rem;
  
  height: 450px;
  background-color: rgb(4, 25, 117);
  color:white
  
}

</style>
