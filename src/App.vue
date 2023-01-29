<script setup>
import { ref } from 'vue';

 const name = 'Hola Proyecto Vue 3 botones con reactividad ejemplo con ref()'
 //se usa ref para hacer reactiva la variable contador
const contador = ref(0);
//se usa const para hacer reactiva la variable contador con una funcion de flecha
const incrementar = () => {
   contador.value++
  console.log('Click 1 incrementar'+contador)
}
</script>

<template>
 <h1>Hola {{ name }}!</h1>
 
 <h2>Incremento de numeros: {{ contador }} </h2>
 <!--Click 1 incrementar-->
  <button @click="incrementar">Click para incrementar</button>
 
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