<script setup>
import { ref, computed } from "vue";

const name = "Vue 3 Desafio final del modulo";

const counter = ref(0);

const ArrayFavorites = ref([]);

const addFavorite = () => {
  ArrayFavorites.value.push(counter.value);
};

const disabledAddBtn = computed(() => {
  const searchNum = ArrayFavorites.value.find((favorite) => favorite === counter.value);
  console.log(searchNum)

  //forma larga de hacer lo mismo
  if (searchNum === 0) return true
  return searchNum ? true : false;
  //Forma mas corta de hacer lo mismo
  // searchNum || searchNum === 0
});

const increment = () => {
    counter.value++;
};

const decrement = () => {
    counter.value--;
};

const reset = () => {
    counter.value = 0;
};

const classCounter = computed(() => {
    if (counter.value === 0) {
        return "zero";
    }
    return counter.value > 0 ? "positive" : "negative";
});

</script>

<template>
  <div class="container text-container mt-2">
    <h1 class="text-center">Hola {{ name }}!</h1>
    <h2 :class="classCounter" class="text-center">
        {{ counter }}
    </h2>
    <div class="btn-group text-center mx-auto">
      <button @click="increment" class="btn btn-success" >Incremet</button>
    <button @click="decrement" class="btn btn-warning">Decrement</button>
    <button @click="reset" class="btn btn-danger">Reset</button>
    <button @click="addFavorite" :disabled="disabledAddBtn" class="btn btn-info">Add to Favorite</button>
    </div>
    
    <br>
    <ul class="list-group mt-3">
      <template v-for="favorite in ArrayFavorites" :key="favorite">
        <li class="list-group-item">
            {{ favorite }}
        </li>
      </template >
        
    </ul>
  </div>
   
</template>

<style>
.negative {
    color: red;
}

.positive {
    color: green;
}

.zero {
    color: black;
}
</style>