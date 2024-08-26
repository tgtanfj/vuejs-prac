<script setup>
import { ref } from 'vue'

const text = ref('')
const select = ref('none')
const checkbox = ref(false)
const radioChecked = ref()
</script>

<template>
  <div>
    <h1>- V-model</h1>
    <input type="text" placeholder="type something" v-model ="text" />
    <p>{{ text }}</p>
    <select v-model="select" id="">
      <option disabled value="">please check</option>
      <option>A</option>
      <option>B</option>
      <option>C</option>
    </select>
    <p>Selected: {{ select }}</p>
    <input type="checkbox" v-model="checkbox" />
    <p>Checked: {{ checkbox }}</p>
    <p>Radio: {{ radioChecked }}</p>
    <input type="radio" v-model="radioChecked" id="A" value="A" />
    <label for="A">A</label>
    <input type="radio" v-model="radioChecked" id="B" value="B" />
    <label for="B">B</label>
  </div>
</template>
