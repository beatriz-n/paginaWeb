<template>
<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/css/bootstrap.min.css" integrity="sha384-MCw98/SFnGE8fJT3GXwEOngsV7Zt27NXFoaoApmYm81iuXoPkFOJwJ8ERdknLPMO" crossorigin="anonymous">
 <div class="row row-coment">
<div class="media-rigth">
    <div class="media-body col-sm-1">
      <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-person-fill" viewBox="0 0 16 16">
        <path d="M3 14s-1 0-1-1 1-4 6-4 6 3 6 4-1 1-1 1H3zm5-6a3 3 0 1 0 0-6 3 3 0 0 0 0 6z"/>
      </svg>
      </div>
    </div>
    <h6 class="coment-font col-sm-1">{{coment}}</h6>
       <button class="btn btn-danger" @click="$emit('remove', coment)">Remover</button>
  </div>
</template>

<script>
export default {
  props: {
    coment: { type: Object, required: true }
  }
}
</script>

<style>
.media-rigth{
  padding-left: 3rem;
}
.row-coment{
align-items: baseline;
padding-left: 20%;
margin: 2rem;
}
.btn-danger{
  height: 2rem;
}

</style>
