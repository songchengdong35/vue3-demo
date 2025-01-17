<template>
  <div>
    <h3 :class="{ redTitle: isRed }">是否成年：{{ isAdult }}</h3>
    <h3>旧值： {{ oldVal }}</h3>
    <button @click="increment">count {{ count }}</button>
  </div>
</template>

<script setup>
import { ref, reactive, computed } from 'vue'

let count = ref(1)
let isRed = ref(false)
const stu = reactive({
  name: 'zx',
  age: 1,
  sex: '男'
})
function increment() {
  count.value++
  stu.age += count.value
  isRed.value = !isRed.value
}
const { name } = stu
console.log('name', name)

// computed
const isAdult = computed(() => {
  return stu.age > 18 ? '是':'否'
})


</script>

<style lang="scss" scoped>
.redTitle {
  color: red
}
</style>
