<script setup>
import { ref, watchEffect } from 'vue'

const x = ref(0)
const y = ref(0)
const sum = ref(0)

watchEffect(() => (sum.value = x.value + y.value))
</script>

<template>
  <h1>- Watch Effect</h1>
  <div>
    <p>x: {{ x }}</p>
    <p>y: {{ y }}</p>
    <p>sum: {{ sum }}</p>
    <button
      @click="
        () => {
          x++
          y++
        }
      "
    >
      click here to increment x & y
    </button>
  </div>
</template>
