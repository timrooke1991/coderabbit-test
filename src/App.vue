<template>
  <div class="app">
    <main class="container">
      <Header />
      <div class="content">
        <Description :content="description" />
        <button @click="count++">Clicked {{ count }} times</button>
        <ul>
          <li v-for="item in items" :key="item">{{ item }}</li>
        </ul>
      </div>
    </main>
  </div>
</template>

<script setup>
import { ref } from "vue";
import Header from "./components/Header.vue";
import Description from "./components/Description.vue";
const description = ref("This is a description");
const count = ref(0);
const items = ref(["Item 1", "Item 2", "Item 3"]);
</script>

<style>
.app {
  min-height: 100vh;
  background-color: #f5f5f5;
  font-family: "Helvetica Neue", sans-serif;
}

.container {
  padding-top: 80px; /* Space for fixed header */
  min-height: calc(100vh - 80px);
  display: flex;
  flex-direction: column;
  align-items: center;
}

.content {
  max-width: 600px;
  margin: 2rem auto;
  padding: 2rem;
  background: white;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  text-align: center;
}

h2 {
  color: #42b983;
  font-family: Arial, sans-serif;
  margin-top: 0;
}

button {
  margin: 20px 0;
  padding: 10px 20px;
  border-radius: 4px;
  border: none;
  background: #42b983;
  color: white;
  cursor: pointer;
  transition: background-color 0.2s ease;
}

button:hover {
  background: #3aa876;
}

ul {
  list-style: none;
  padding: 0;
}

li {
  margin: 10px 0;
  padding: 8px;
  background: #f8f8f8;
  border-radius: 4px;
}
</style>
