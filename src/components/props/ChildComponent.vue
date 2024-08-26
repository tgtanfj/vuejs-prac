<script setup>
  const props = defineProps(['props1'])
</script>

<template >
  <div style="border: 3px solid red">
    <h3>Child component</h3>
    <div>
      This is props from parent: {{ props.props1 }} 
    </div>
  </div>
</template>