<script setup>
import { ref } from 'vue';
import ChildComponent from './props/ChildComponent.vue';

  const props1 = ref("")

</script>

<template>
  <h1>- Passing Props</h1>
  <div style="border: 3px solid blue; padding: 20px;">
    <h3>This is parent component</h3>
    <input type="text" v-model="props1" placeholder="type something">
    <ChildComponent :props1="props1"/>
  </div>
</template>
