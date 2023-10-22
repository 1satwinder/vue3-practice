<script setup>
import { reactive, computed, ref, watch } from 'vue';
import { RouterLink } from 'vue-router';
import '../assets/example.css';


const data = reactive({
  count: 0,
  name: 'satwinder',
  scores: [12, 14, 39]
});

const title = ref('Vue Practice');

const isWinner = computed(() => data.counter >= 5);
const titleLength = computed(() => title.value.length);

const question = ref('')
const answer = ref('Questions usually contain a question mark. ;-)')

// watch works directly on a ref
watch(question, async (newQuestion, oldQuestion) => {
  if (newQuestion.indexOf('?') > -1) {
    answer.value = 'Thinking...'
    try {
      const res = await fetch('https://yesno.wtf/api')
      answer.value = (await res.json()).answer
    } catch (error) {
      answer.value = 'Error! Could not reach the API. ' + error
    }
  }
})


</script>

<template>
  <p class="red-color">Text with red color with css import</p> <!-- red-color coming from global style main.css -->

  <p>Name is {{ data.name }}</p>
  <p>Count is {{ data.count }}</p>
  <p>Winner is {{ isWinner }}</p>

  <input v-model="data.name" type="text" width="100px" />
  <hr>
  <button @click="data.count += 1">incremanrt count</button>
  <br><br><br>

  <h4>Title {{ title }} length {{ titleLength }}</h4>
  <br>

  <p>
    Ask a yes/no question:
    <input v-model="question" />
  </p>
  <p>{{ answer }}</p>
  

  <h4>Router</h4>
  <a href="/about">about page with anchor tag</a>
  <hr>
  <RouterLink to="/about"> about page with vue router</RouterLink>
</template>

<style>
.blue-color {
  color: blue;
}
</style>
