<script setup>
const sayHi1 = () => {
  alert('một')
}
const sayHi2 = () => {
  alert('hai')
}
const submitForm = () => {
  alert('submit')
}
</script>

<template>
  <h1>- Events In Vue</h1>
  <h3>Event bubbling (chưa xử lí)</h3>
  <button @click="sayHi1">
    một
    <button @click="sayHi2">hai</button>
  </button>
  <h3>Sau khi xử lí bằng .stop</h3>
  <button @click="sayHi1">
    một
    <button @click.stop="sayHi2">hai</button>
  </button>
  <h3>Event submit form</h3>
  <form @submit.prevent.stop="submitForm">
    <input
      type="text"
      placeholder="type something and press alt+enter to submit"
      @keyup.enter.alt="submitForm"
    />
    <button type="submit">submit form</button>
  </form>
</template>
