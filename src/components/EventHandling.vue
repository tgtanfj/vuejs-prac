<script setup>
import { ref } from 'vue'

const value = ref('')
const number = ref(0)

const submitAlert = () => {
  alert(`This is value: ${value.value}`)
}
</script>

<template>
  <h1>- Event Handling</h1>
  <div>
    <input
      style="width: 500px"
      placeholder="type something then press enter"
      :value="value"
      @input="(e) => (value = e.target.value)"
      type="text"
      @keydown.enter="submitAlert"
    />
  </div>
  <div style="margin-top: 10px">
    <button @click="number += 1">add number</button>
    <span>{{ number }}</span>
  </div>
</template>
