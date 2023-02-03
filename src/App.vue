<script>
export default {
  name: 'App',
  data() {
    return {
      count: 0
    }
  },
  methods: {
    increment() {
      this.count++
    }
  }
}

</script>
<template>

    <h1>Wellcome to Fourth Module of Vue 3 Course API de Opciones u Option API</h1>
    
    <button @click="increment">{{ count }}</button>
    
     </template>

<!--<script >
import { ref } from 'vue'

export default {
  // `setup` is a special hook dedicated for composition API.
  setup() {
    const count = ref(0)

    function increment() {
      count.value++
    }

    // expose the state to the template
    return {
      count,
      increment
    }
  }
}

</script>-->

