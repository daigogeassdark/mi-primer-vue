<script setup>
 const name = 'Hola Proyecto Vue 3 v-on ejemplos '

const click1 = (message) => {
  console.log(message)
}
const click2 = (message) => {
  console.log(message)
}
</script>

<template>
 <h1>Hola {{ name }}!</h1>
 <!--Click 1 avreviado-->
  <button @click="click1('mensaje 1')" class="btn btn-info">Click1</button>
  <!--Click 2 completo-->
  <button v-on:click="click2('mensaje 2')" class="btn btn-sucess">Click2</button>
</template>
<style>
button{
  margin: 10px;
  color:green;
  border: 1px solid red;
  border-radius: 25%!important;
  width:90px!important;
  height: 40px!important; ;

}
h1 {
  color: red;
}
</style>