<template>
    <div class="card p-3">
        <img  :src="poster" class="card-img-top" :alt="nome">
      <div class="card-body text-center">
          <h5 class="card-title">{{nome}}</h5>
          <h3 class="card-title">{{titolo}}</h3>
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


<style scoped lang="scss">

.card{
  background-color: rgb(4, 25, 117);
  width: 15rem;
}

</style>
