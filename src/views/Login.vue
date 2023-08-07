<template>
    <div class="flex justify-center items-center h-screen">
      <form @submit.prevent="login">
        <input v-model="email" type="email" placeholder="Email" class="p-2 m-1 border" />
        <input v-model="password" type="password" placeholder="Password" class="p-2 m-1 border" />
        <button type="submit" class="bg-blue-500 text-white p-2 m-1">Login</button>
      </form>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  import { useRouter } from 'vue-router';
  
  const email = ref('');
  const password = ref('');
  const router = useRouter();
  
  const login = () => {
    router.push('/welcome');
  };
  </script>
  
  <style scoped>
  </style>
  