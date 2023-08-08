<template>
    <div class="min-h-screen flex items-center justify-center bg-gray-100">
      <div class="max-w-md p-6 bg-white rounded-lg shadow-md">
        <h2 class="text-2xl mb-4">Register</h2>
        <form @submit.prevent="register">
          <div class="mb-3">
            <label for="registerUsername">Username:</label>
            <input type="text" v-model="registerUsername" id="registerUsername" class="w-full p-2 border rounded" />
          </div>
          <div class="mb-3">
            <label for="registerPassword">Password:</label>
            <input type="password" v-model="registerPassword" id="registerPassword" class="w-full p-2 border rounded" />
          </div>
          <button type="submit" class="bg-blue-500 text-white px-4 py-2 rounded">Register</button>
        </form>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        registerUsername: '',
        registerPassword: '',
      };
    },
    methods: {
      register() {
        // Your registration logic here
        // Simulate successful registration for demonstration
        const user = {
          username: this.registerUsername,
          password: this.registerPassword,
        };
        this.$root.state.users.push(user);
        this.$router.push('/login');
      },
    },
  };
  </script>
  