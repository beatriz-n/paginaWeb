<template>
<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/css/bootstrap.min.css" integrity="sha384-MCw98/SFnGE8fJT3GXwEOngsV7Zt27NXFoaoApmYm81iuXoPkFOJwJ8ERdknLPMO" crossorigin="anonymous">
<div class="row">
<div class="card-espace">
<div class="card col" style="width: 18rem;">
<img class="card-img-top" src="../assets/logo.png" alt="Card image cap">
<div class="card-body">
    <h5 class="card-title">{{title}}</h5>
  </div>
  <p class="card-text">{{card}}</p>
  </div>
  </div>
  </div>
</template>

<script>
export default {
  props: {
    title: { type: Object, required: true },
    card: { type: Object, required: true }
  }
}
</script>

<style>
.card-espace{
  margin-top: 5%;
  margin-left: 50%;
}
</style>
