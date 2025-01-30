<template>
  <div>
      <AnimalCard v-for="animal in animals" :key="animal.name" :animal="animal" />
      <LogIn :message="message" />
  </div>
</template>

<script setup>
import AnimalCard from '@/components/AnimalCards.vue';
import LogIn from '@/components/LogIn.vue';
const message = "Hello World!";
const animals = [{name: "Walrus", image: "url"}, {name: "Mark Fridlin", image: "url1"}];

</script>

<style scoped>

</style>