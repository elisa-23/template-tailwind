<template>
    <div>
        <form action="submit">
            <input type="text" v-model="user.username" placeholder="Enter a Username">
            <input type="text" v-model="user.password" placeholder="Enter a Username">
            <button type="submit" @click="signUp">Sign Up</button>
        </form>
    </div>
</template>

<script setup>
let user = {username: "", password: ""};
function signUp() {
    console.log(user)
}
</script>

<style scoped>

</style>