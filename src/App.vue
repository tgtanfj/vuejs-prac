<script setup>
import BindingClass from './components/BindingClass.vue'
import BindingStyle from './components/BindingStyle.vue'
import EventHandling from './components/EventHandling.vue';
import VFor from './components/VFor.vue';
import VIfAndVShow from './components/VIfAndVShow.vue'
</script>

<template>
  <div>
    <VIfAndVShow />
    <BindingClass />
    <BindingStyle />
    <VFor/>
    <EventHandling/>
  </div>
</template>

<style scoped></style>
