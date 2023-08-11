<script setup>
// COMPOSITION API style
import { reactive } from 'vue';

const user = reactive({
        name: '',
        email: '',
        password: ''
})

const register = () => {
    console.log(user)
}
</script>

<template>
    <h2>Register Here</h2>
    <form @submit.prevent="register()">
        <input type="text" placeholder="Name" v-model="user.name" />
        <input type="email" placeholder="Email" v-model="user.email" />
        <input type="password" placeholder="Password" v-model="user.password" />
        <input value="Register" type="submit" />
    </form>
</template>

<style scoped>
h2 {
    text-align: center;
}

form {
    display: flex;
    flex-direction: column;
    align-items: center;
    align-content: center;
}

form input {
    margin: 10px;
}
</style>