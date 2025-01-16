<template>
    <div>
        <form @submit.prevent="signUp">
            <label for="username">Username: </label>
            <input type="text" id="username" v-model="user.username" placeholder="Enter a Username">
            <br>
            <label for="password">Password: </label>
            <input type="password" id="password" v-model="user.password" placeholder="Enter a Password">
            <br>
            <button action="submit">Sign Up</button>
        </form>
    </div>
</template>

<script setup>
import { reactive } from 'vue';

let user = reactive({username: "", password: ""});
function signUp() {
    console.log(user.username, user.password);
}

</script>

<style scoped>

</style>