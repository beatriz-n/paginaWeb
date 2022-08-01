<template>
<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/css/bootstrap.min.css" integrity="sha384-MCw98/SFnGE8fJT3GXwEOngsV7Zt27NXFoaoApmYm81iuXoPkFOJwJ8ERdknLPMO" crossorigin="anonymous">
  <div class="row">
  <div class="col-sm-11">
    <img class="logo" alt="Vue logo" src="./assets/logo.png">
  </div>
  <div class="col-sm-1">
    <button type="button" class="btn btn-default"><b>Login</b></button>
  </div>
</div>
<div class="container-fluid center">
  <h3>Exemplo de pagina com Vuejs</h3>
  <p>Bem-vindo</p>
</div>
<div class="media">
    <div class="media-left">
      <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-chat" viewBox="0 0 16 16">
  <path d="M2.678 11.894a1 1 0 0 1 .287.801 10.97 10.97 0 0 1-.398 2c1.395-.323 2.247-.697 2.634-.893a1 1 0 0 1 .71-.074A8.06 8.06 0 0 0 8 14c3.996 0 7-2.807 7-6 0-3.192-3.004-6-7-6S1 4.808 1 8c0 1.468.617 2.83 1.678 3.894zm-.493 3.905a21.682 21.682 0 0 1-.713.129c-.2.032-.352-.176-.273-.362a9.68 9.68 0 0 0 .244-.637l.003-.01c.248-.72.45-1.548.524-2.319C.743 11.37 0 9.76 0 8c0-3.866 3.582-7 8-7s8 3.134 8 7-3.582 7-8 7a9.06 9.06 0 0 1-2.347-.306c-.52.263-1.639.742-3.468 1.105z"/>
</svg>
    </div>
    <div class="media-body">
      <h4 class="media-heading">Comente:</h4>
      <form  @submit.prevent="addTodo(coment)">
     <input type="text" class="form-input" placeholder="comente algo!">
     <button>Comentar</button>
     </form>
      <hr>
    </div>
  </div>
<ListComent v-for="c in coments" :key="c.id"/>
</template>
<script>
import ListComent from './components/list-coment.vue'

export default {
  name: 'App',
  components: { ListComent },
  data () {
    return { coments: [], todo: { checked: false } }
  },
  methods: {
    addTodo (coment) {
      coment.id = Date.now()
      this.coments.push(coment)
      this.coment = { checked: false }
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

</style>

<style scoped>
.logo{
  width:3rem;
}
.btn-default{
  width: 5rem;
  background-color: rgb(107, 155, 107);
}
.center{
  text-align: center;
  padding: 3rem;
  background-color: rgb(140, 150, 130);
  width: auto;
  margin: 2rem;
}
.media{
  padding: 2rem;
}
.media-left{
  padding-right: 1rem;
}
.form-input{
  width: 50%;
}
.media-rigth{
  padding-left: 10%;
  font-size: small;
}
</style>
