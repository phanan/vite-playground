<template>
  <app-header/>
  <p>Click the button and delete this element in the code.</p>
  <p>
    <span>Count is: {{ count }}</span>
    <button @click="count++">increment</button>
  </p>
</template>

<script>
import { defineAsyncComponent, reactive } from 'vue'
import AppHeader from './components/Header.vue'

export default {
  components: {
    AppHeader
  },

  setup () {
    const state = reactive({
      count: 0
    })

    return {
      ...state
    }
  }
}
</script>

<style scoped>
h1 {
  color: #4fc08d;
}

h1, p {
  font-family: Arial, Helvetica, sans-serif;
}
</style>
