<template>
    <div>
        <h2>Hi</h2>
    </div>
</template>

<script setup>
import {ref, onMounted} from 'vue';
import {useRoute} from 'vue-router';

const route = useRoute();
const pokemon = ref("");

async function getPokemon(){
    let res = await fetch(`https://pokeapi.co/api/v2/pokemon/${route.params.index}`);
    let data = await res.json();
    pokemon.value = data;
}

onMounted(() => {
    getPokemon();
})
</script>

<style lang="scss" scoped>

</style>