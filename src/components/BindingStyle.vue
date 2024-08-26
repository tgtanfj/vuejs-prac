<script setup>
import { reactive, ref } from 'vue'

const object = reactive({
  color: 'red',
  background: 'yellow'
})

const paddingOj = reactive({
  padding: '20px'
})

const textpx = ref(20)
const color = ref('blue')
</script>

<template>
  <h1>- Binding Class</h1>
  <div :style="object">hello</div>
  <div
    :style="{
      color,
      fontSize: textpx + 'px'
    }"
  >
    hello 2
  </div>
  <div
    :style="[
      {
        color,
        fontSize: textpx + 'px',
        background: 'gray'
      },
      paddingOj
    ]"  
  >
    hello 3
  </div>
</template>
