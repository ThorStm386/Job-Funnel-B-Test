<template>
  <div class="container">
    <h1>Page Title</h1>

   
    <div>
      <p>Count: {{ count }}</p>
      <button @click="count++">+</button>
      <button @click="count--">-</button>
    </div>

    <!-- Navigation -->
    <nav>
      <NuxtLink to="/">Home</NuxtLink> |
      <NuxtLink to="/about">About</NuxtLink>
    </nav>

    <!-- Render child pages here -->
    <NuxtPage />
  </div>
</template>

<script setup>
import { ref } from 'vue'
  const {id} = useRoute().params

const count = ref(0)
</script>

<style scoped>
.container {
  text-align: center;
  margin-top: 50px;
}
button {
  margin: 5px;
  padding: 8px 12px;
  background: #0070f3;
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}
button:hover {
  background: #005bb5;
}
nav {
  margin-top: 20px;
}
nav a {
  margin: 0 10px;
  text-decoration: none;
  color: #0070f3;
}
nav a:hover {
  text-decoration: underline;
}
</style>
