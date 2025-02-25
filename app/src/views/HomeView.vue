<template>
    <div>
        <card v-for="(mon, index) in pokemon" 
        :key="mon.name" 
        :mon="mon" 
        :index="index + 1"/>
    </div>
</template>

<script setup>
import { ref, onMounted } from "vue";
import card from '@/components/Cards.vue';
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