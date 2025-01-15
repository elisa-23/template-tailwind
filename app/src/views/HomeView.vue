<!-- get it through vbase-3-setup (type out the whole thing) -->


<!-- counter window -->
<template>
    <h1>{{ count }}</h1>
    <button @click="increment">Click Me</button>
</template>

<script setup>
import { ref } from "vue";


let count = ref(0);     //also works without semicolons
function increment() {
    count.value++;
}

</script>

<style scoped>

</style>