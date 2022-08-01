<template>
<div class="card-espace">
<div class="card" style="width: 18rem;">
<img class="card-img-top" src="./assets/logo.png" alt="Card image cap">
<div class="card-body">
    <h5 class="card-title">{{title}}</h5>
    <p class="card-text">{{card}}</p>
    <a href="#" class="btn btn-primary">Go somewhere</a>
  </div>
  </div>
  </div>
</template>

<script>
export default {
  props: {
    card: { type: Object, required: true },
    title: { type: Object, required: true }
  }
}
</script>
