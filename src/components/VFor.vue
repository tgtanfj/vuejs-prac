<script setup>
import { ref } from 'vue'

const object = ref([
  1,44,56,7,34
])

const addRandomNumber = () => {
  object.value.push(Math.floor(Math.random() * 100))
}

</script>

<template>
  <h1>- V-for</h1>
  <div>
    <button @click="addRandomNumber">add random number</button>
    <p>Only show number less than 50</p>
    <ul>
      <template v-for="(value, key) in object">
        <li v-if="value < 50" :key="key">
          {{ value }}
        </li>
      </template>
    </ul>
  </div>
</template>
