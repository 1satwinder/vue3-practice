<template>
    <h1>In side hello world file {{ counter }}</h1>
    <button @click="updateCounter(10)">Increament</button>
</template>

<script setup>
import { ref, onMounted } from 'vue';
const props = defineProps(['counter']);
const emit = defineEmits(['updateCounter'])
console.log('props are', props);

const counter = ref(props.counter);

function updateCounter(step) {
    counter.value += step;
    emit('updateCounter',step);
}

onMounted(() => {
    console.log('counter is', counter.value);
})

</script>