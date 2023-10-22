<template>
  <div class="about">
    <h1>This is an about page {{ name }} </h1>
    <button @click="changeName"> changeName </button>
  </div>
</template>

<script setup>
import { onMounted, ref } from 'vue';

const name = ref('mounted');

onMounted(() => {
  console.log('about page is mounted');
  name.value = 'satwinder'
})

const changeName = () => {
  name.value += 'talwinder'
}

</script>

<style>
</style>
