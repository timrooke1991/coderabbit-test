<template>
  <div class="container">
    <div class="content">
      <h1>{{ message }}</h1>
      <p>{{ description }}</p>
      <button @click="count++">Clicked {{ count }} times</button>
      <ul>
        <li v-for="item in items" :key="item">{{ item }}</li>
      </ul>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";

const message = ref("Hello World!");
const description = ref("This is a description");
const count = ref(0);
const items = ref(["Item 1", "Item 2", "Item 3"]);
</script>

<style>
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

h1 {
  color: #42b983;
  font-family: Arial, sans-serif;
}
div {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.content {
  max-width: 600px;
  margin: 0 auto;
}

button {
  margin: 20px 0;
  padding: 10px 20px;
  border-radius: 4px;
  border: none;
  background: #42b983;
  color: white;
  cursor: pointer;
}

ul {
  list-style: none;
  padding: 0;
}

li {
  margin: 10px 0;
}
</style>
