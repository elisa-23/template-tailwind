<template>
    <RouterLink :to="pkmnPath">
            <h2>{{ mon.name }}</h2>
            <h3>{{ index }}</h3>
    </RouterLink>
</template>

<script setup>
import { computed } from 'vue';
const props = defineProps (
    {mon: Object, index: String}
)

const pkmnPath = computed(() =>{
    return `/Pokemon/${props.index}`;
})
</script>

<style lang="scss" scoped>

</style>