<script lang="ts">
import { defineComponent, ref } from 'vue'

export default defineComponent({
  name: 'HelloWorld',
  props: {
    msg: {
      type: String,
      required: true
    }
  },
  setup() {
    const count = ref(0)
    const increment = () => {
      count.value++
    }

    return { count, increment }
  }
})
</script>

<template>
  <h1>{{ msg }}</h1>
  <button @click="increment">Count is: {{ count }}</button>
</template>

<style scoped>
/* Ваши стили */
</style>