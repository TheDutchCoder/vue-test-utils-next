<script setup lang="ts">
// imported components are also directly usable in template
import { ref } from 'vue'
import Hello from './Hello.vue'

const count = ref(0)
const inc = () => {
  count.value++
}

defineExpose({
  count
})
</script>

<template>
  <button @click="inc">{{ count }}</button>
  <Hello />
</template>
