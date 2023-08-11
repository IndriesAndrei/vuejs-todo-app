<script setup>
import { ref } from 'vue'
let isLoggedIn = ref(false)

const login = () => {
    isLoggedIn.value = true
    console.log(isLoggedIn)
}

const logout = () => {
    isLoggedIn.value = false
    console.log(isLoggedIn)
}
</script>

<template>
    <!-- Conditionally render elements -->
    <div v-if="isLoggedIn ">
        <h3 class="welcome-text">Welcome User</h3>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsam quis ullam quidem itaque reprehenderit dolorem placeat, ab sint perferendis porro.</p>
    </div>
    <div v-else>
        <h3 class="danger-text">Thank You</h3>
        <p>Ipsam quis ullam quidem itaque reprehenderit dolorem placeat, ab sint perferendis porro. Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
    </div>
    <div>
        <button @click="login()" v-if="!isLoggedIn">Login</button>
        <button @click="logout()" v-else>Logout</button>
    </div>
</template>

<style scoped>
.welcome-text {
    color: green;
}
.danger-text {
    color: red;
}
</style>