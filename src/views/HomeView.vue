<template>
  <main>
    <button @click="increment">count {{ count }}</button>
  </main>
</template>

<script setup>
import { ref } from 'vue'

let count = ref(0)
function increment() {
  count.value++
  console.log('increment', count.value)
}
</script>

<style lang="less" scoped>

</style>
