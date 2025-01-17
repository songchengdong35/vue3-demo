<template>
  <main>
    <button @click="increment">count {{ count }}</button>
  </main>
</template>

<script setup>
import { ref, reactive } from 'vue'

let count = ref(0)
const stu = reactive({
  name: 'zx',
  age: 38,
  sex: '男'
})
function increment() {
  count.value++
  stu.age += count.value
}
const { name } = stu
console.log('name', name)
</script>

<style lang="less" scoped>

</style>
