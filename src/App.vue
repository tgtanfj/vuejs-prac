<script setup>
import BindingClass from './components/BindingClass.vue'
import BindingStyle from './components/BindingStyle.vue'
import EventHandling from './components/EventHandling.vue'
import LifeCycleHook from './components/LifeCycleHook.vue'
import VFor from './components/VFor.vue'
import VIfAndVShow from './components/VIfAndVShow.vue'
import WatchersInVueJS from './components/WatchersInVueJS.vue'
</script>

<template>
  <div>
    <VIfAndVShow />
    <BindingClass />
    <BindingStyle />
    <VFor />
    <EventHandling />
    <LifeCycleHook />
    <WatchersInVueJS />
  </div>
</template>

<style scoped></style>
