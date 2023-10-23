<template>
  <div class="about">
    <h1>This is an about page {{ name }} </h1>
    <button @click="changeName"> changeName </button>
    <br><br>
    <p>Counter Updates by child by emitting events {{ counterInRoot }}</p>
    <HelloWorld :counter="counterInRoot" @updateCounter="updateCounter"></HelloWorld>
  </div>
</template>

<script setup>
import { onMounted, ref } from 'vue';
import HelloWorld from '@/components/HelloWorld.vue';

const name = ref('mounted');
const counterInRoot = ref(0);

function updateCounter(increamentBy) {
  counterInRoot.value += increamentBy;
}

onMounted(() => {
  console.log('about page is mounted');
  name.value = 'satwinder'
})

const changeName = () => {
  name.value += 'talwinder'
}

</script>

<style></style>
