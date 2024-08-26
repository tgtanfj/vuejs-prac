<script setup>
import { ref, watch } from 'vue'

const question = ref('')
const answer = ref('Questions usually contain a question mark. ;-)')
const loading = ref(false)

watch(question, async (newQuestion, oldQuestion) => {
  console.log('check')
  if (newQuestion.includes('?')) {
    loading.value = true
    answer.value = 'Thinking...'
    try {
      const res = await fetch('https://yesno.wtf/api')
      answer.value = (await res.json()).answer
      console.log(oldQuestion)
    } catch (error) {
      answer.value = 'Error! Could not reach the API. ' + error
    } finally {
      loading.value = false
    }
  }
})
</script>

<template>
  <h1>- Watch</h1>
  <p>gần giống useEffect</p>
  <p>watch(a,callback): callback b sẽ được chạy khi a thay đổi</p>
  <p>
    Ask a yes/no question:
    <input placeholder="Do you wanna play?" v-model="question" :disabled="loading" />
  </p>
  <p>{{ answer }}</p>
</template>
