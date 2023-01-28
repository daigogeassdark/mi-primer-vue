<script setup>
 const name = 'Hola Proyecto Vue 3 v-for y v-if + template'
 const arrayFrutas = [
    {
        name: "Manzana",
        price: "$1.00",
        description: "Una manzana",
        stock: 0,
    },
    {
        name: "Pera",
        price: "$2.00",
        description: "Una pera",
        stock: 10,
    },
    {
        name: "Naranja",
        price: "$3.00",
        description: "Una naranja",
        stock: 20,
    },
];
</script>

<template>
 <h1>Hola {{ name }}!</h1>
  <ul>
      <template v-for="item in arrayFrutas" :key="item.name">
        <li  v-if="item.stock > 0 ">
          {{ item.name }} - {{ item.price }} - {{ item.description }} - {{ item.stock }}
        </li>
      </template>    
  </ul>
</template>
<style>
h1 {
  color: red;
}
</style>