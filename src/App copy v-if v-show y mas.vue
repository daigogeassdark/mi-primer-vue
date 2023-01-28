<script setup>
 const msg = 'Hola Proyecto Vue 3'
 const styleColor = 'color:yellow'
 const arrayColores = ['red', 'blue', 'green']
 const active = true
</script>

<template>
  <h1>Saludo: {{ msg.toUpperCase() }}</h1>
  <h2 v-bind:style="styleColor">Hola Con color</h2>
  <h2 :style="`color: ${arrayColores[2]}`">Hola no soy azul</h2>
  <h2>{{ active ? 'Toy vivo' : 'Falta todavia' }}</h2>

  <h2 v-if="active">Hola estoy activo en la jugada</h2>
  <h2 v-else>Ya no esta activo en la jugada</h2>
  <h2 v-show="active">No deberia verme</h2>
  <!--<h2 v-if="!active">Ya no esta activo en la jugada</h2>-->
</template>
<style>
h1 {
  color: red;
}
</style>