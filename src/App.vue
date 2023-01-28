<script setup>
 const name = 'Hola Proyecto Vue 3 vfor objetos'
 const arrayFrutas =  {
            name: "Manzana",
            price: "$1.00",
            description: "Una manzana",
        }
 
</script>

<template>
 <h1>Hola {{ name }}!</h1>
  <ul>
    <li v-for="(value, propiedad, index) in arrayFrutas " :key="value" >
      {{ index }} - {{ propiedad }}: {{ value }}
    </li>
  </ul>
</template>
<style>
h1 {
  color: red;
}
</style>