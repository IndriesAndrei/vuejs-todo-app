<script setup>
import { RouterView } from 'vue-router'
import TodoHeader from './components/TodoHeader.vue'
import Register from './components/Register.vue'
import AuthenticationUser from './components/AuthenticationUser.vue';
import UserList from './components/UserList.vue';
</script>

<template>
  <TodoHeader />
  <RouterView />
  <Register />
  <AuthenticationUser />
  <UserList />
</template>

<style lang="scss">
* {
  font-family: sans-serif;
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.container {
  max-width: 1100px;
  margin: 0 auto;
}
</style>
