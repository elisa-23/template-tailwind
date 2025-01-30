<template>
    <div>
        <AnimalCard v-for="animal in animals" :key="animal.name" :animal="animal" />
    </div>
</template>

<script setup>
import AnimalCards from '@/components/AnimalCards.vue';
const animals = [{name: "Walrus", image: "url"}, {name: "Mark Fridlin", image: "url1"}];
</script>

<style scoped>

</style>