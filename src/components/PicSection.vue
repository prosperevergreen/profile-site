<template>
  <div class="container-fluid d-flex justify-content-center">
    <img class="demo" :src="require(`@/assets/images/${image}`)" alt="Tic-Tac-Toe gif Image">
  </div>
</template>

<script>
export default {
  props:{
    image: String
  }
}
</script>

<style>
.demo{
  height: 50vh;
}

</style>