<script setup>
import BindingClass from './components/BindingClass.vue'
import BindingStyle from './components/BindingStyle.vue'
import EventHandling from './components/EventHandling.vue'
import EventsInVueJS from './components/EventsInVueJS.vue'
import LifeCycleHook from './components/LifecycleHook.vue'
import PassingProps from './components/PassingProps.vue'
import VFor from './components/VFor.vue'
import VIfAndVShow from './components/VIfAndVShow.vue'
import VmodelInVueJS from './components/VmodelInVueJS.vue'
import WatchersInVueJS from './components/WatchersInVueJS.vue'
</script>

<template>
  <div>
    <VIfAndVShow />
    <BindingClass />
    <BindingStyle />
    <VFor />
    <VmodelInVueJS />
    <EventHandling />
    <LifeCycleHook />
    <WatchersInVueJS />
    <PassingProps />
    <EventsInVueJS />
  </div>
</template>

<style scoped></style>
