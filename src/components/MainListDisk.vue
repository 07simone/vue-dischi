<template>
    <div class="card p-3" style="width: 15rem;">
        <img  :src="poster" class="card-img-top" alt="...">
      <div class="card-body text-center">
          <h5 class="card-title">{{titolo}}</h5>
          <h3 class="card-title">{{nome}}</h3>
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
  background-color: lightseagreen;
}

</style>
