<!-- must name files in two words b/c html elements are one word and these get compiled into the html later ==> might lead to conflicts -->

<template>
    <div>
        <h2 v-for="animal in animals" :key="animal">{{ animal }}</h2>       <!-- iterates through the array animals -->
    </div>
</template>

<script setup> 
const animals = ["Zebra", "Panda", "Mark", "Whale"]
</script>

<style scoped>

</style>