<script setup>
import { ref } from 'vue'

const blue = ref(false)
const isVisible = ref(false)

const toggleVisible = () => {
  isVisible.value = !isVisible.value
}

const toggleIsBlue = () => {
  blue.value = !blue.value
}
</script>

<template>
  <h1>- v-if v-else v-show</h1>
  <button @click="toggleIsBlue">toggle blue</button>
  <h1 v-if="blue" style="color: blue">Blue</h1>
  <h1 v-else>Blue</h1>
  <br />
  <button @click="toggleVisible">toggle visible</button>
  <h1 v-show="isVisible">Visible</h1>
</template>
