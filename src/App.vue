<script >
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

</script>
 <template>

<h1>Wellcome to Fourth Module of Vue 3 Course; Reactividad sin atributo Setup</h1>

<button @click="increment">{{ count }}</button>

 </template>
