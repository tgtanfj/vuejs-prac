<script setup>
import { ref } from 'vue'

const value = ref('')
const number = ref(0)
const isChecked = ref(false)
const selected = ref("")

const submitAlert = () => {
  alert(`This is value: ${value.value}`)
}
</script>

<template>
  <h1>- Event Handling & Form Input Binding</h1>
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
  <div style="margin-top: 10px">
    <input v-model="isChecked" type="checkbox" />
    check: {{ isChecked }}
  </div>
  <div style="margin-top: 10px">
    <div>Selected: {{ selected }}</div>

    <select v-model="selected">
      <option disabled value="">Please select one</option>
      <option>A</option>
      <option>B</option>
      <option>C</option>
    </select>
  </div>
</template>
