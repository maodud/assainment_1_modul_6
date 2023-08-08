<template>
    <div class="min-h-screen flex items-center justify-center bg-gray-100">
      <div class="max-w-md p-6 bg-white rounded-lg shadow-md">
        <h2 class="text-2xl mb-4">Welcome, {{ $root.state.currentUser.username }}!</h2>
        <button class="bg-blue-500 text-white px-4 py-2 rounded" @click="logout">Logout</button>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    methods: {
      logout() {
        this.$root.state.currentUser = null;
        this.$router.push('/login');
      },
    },
  };
  </script>
  