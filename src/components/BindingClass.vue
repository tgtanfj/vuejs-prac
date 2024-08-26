<script setup>
import { ref } from 'vue'

const isActive = ref(true)
const error = ref(true)

// const classObject = reactive({
// 	active: true,
// 	error: true
// })
</script>

<template>
  <h1>- Binding Class</h1>
  <button class="button" style="margin-bottom: 10px" :class="{ active: isActive, error: error }">
    button
  </button>
  <!-- <button class="button" style="margin-bottom: 10px;" :class="classObject">button</button> -->
  <br />
  <button @click="isActive = !isActive">toggle active</button>
  <button @click="error = !error">toggle error</button>
</template>

<style>
.active {
  border: none;
  background-color: #61a9e4;
  width: 5rem;
  height: 2rem;
  border-radius: 4rem;
  color: white;
  &:hover {
    background-color: #3791ed;
  }
}
.button {
  border: none;
  background-color: #a1a1a1;
  width: 5rem;
  height: 2rem;
  color: white;
  border-radius: 4rem;
  &:hover {
    background-color: #3791ed;
  }
}
.error {
  border: none;
  background-color: #ea2749;
  width: 5rem;
  height: 2rem;
  color: white;
  border-radius: 4rem;
  &:hover {
    background-color: #ea2749;
  }
}
</style>
