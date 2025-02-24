<template>
    <div>
        <div v-for="(mon, index) in pokemon" :key="mon.name">
            <h2>{{ mon.name }}</h2>
            <h3>{{ index + 1 }}</h3>
        </div>
    </div>
</template>

<script setup>
import { ref, onMounted } from "vue";
const pokemon = ref('');
async function getPokemon() {
    let res = await fetch("https://pokeapi.co/api/v2/pokemon/?limit=151");
    let data = await res.json();
    pokemon.value = data.results;
}
onMounted(() => {
    getPokemon();
});
</script>

<style lang="scss" scoped>

</style>