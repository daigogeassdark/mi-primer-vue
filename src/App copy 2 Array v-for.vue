<script setup>
 const name = 'Hola Proyecto Vue 3'
 const arrayFrutas = [ {
            name: "Manzana",
            price: "$1.00",
            description: "Una manzana",
        },
        {
            name: "Pera",
            price: "$2.00",
            description: "Una pera",
        },
        {
            name: "Naranja",
            price: "$3.00",
            description: "Una naranja",
        },];
</script>

<template>
 <h1>Hola {{ name }}!</h1>
  <ul>
    <li v-for="(fruta, index) in arrayFrutas" :key="fruta.name">
     Código de Fruta: {{ index }} <br> Nombre de la fruta: {{ fruta.name }} - Precio: {{ fruta.price }} - Descripción: {{ fruta.description }}
    </li>
  </ul>
</template>
<style>
h1 {
  color: red;
}
</style>