<template>
    <div class="min-h-screen flex items-center justify-center bg-gray-100">
      <div class="max-w-md p-6 bg-white rounded-lg shadow-md">
        <h2 class="text-2xl mb-4">Login</h2>
        <form @submit.prevent="login">
          <div class="mb-3">
            <label for="loginUsername">Username:</label>
            <input type="text" v-model="loginUsername" id="loginUsername" class="w-full p-2 border rounded" />
          </div>
          <div class="mb-3">
            <label for="loginPassword">Password:</label>
            <input type="password" v-model="loginPassword" id="loginPassword" class="w-full p-2 border rounded" />
          </div>
          <button type="submit" class="bg-blue-500 text-white px-4 py-2 rounded">Login</button>
        </form>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        loginUsername: '',
        loginPassword: '',
      };
    },
    methods: {
      login() {
        // Your login logic here
        // Simulate successful login for demonstration
        const user = {
          username: this.loginUsername,
          password: this.loginPassword,
        };
        this.$root.state.currentUser = user;
        this.$router.push('/welcome');
      },
    },
  };
  </script>
  