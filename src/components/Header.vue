<template>
  <header class="header">
    <div class="header-content">
      <h1 class="logo">{{ title }}</h1>
      <nav class="nav">
        <ul>
          <li v-for="item in menuItems" :key="item.text">
            <a href="#" @click.prevent="handleNavClick(item.text)">{{
              item.text
            }}</a>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script setup>
import { ref } from "vue";

const title = ref("Vue Demo");
const menuItems = ref([
  { text: "Home" },
  { text: "About" },
  { text: "Contact" },
]);

const handleNavClick = (text) => {
  console.log(`Clicked: ${text}`);
};
</script>

<style scoped>
.header {
  background: #ffffff;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 1000;
}

.header-content {
  max-width: 1200px;
  margin: 0 auto;
  padding: 1rem 2rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo {
  color: #42b983;
  margin: 0;
  font-size: 1.5rem;
  font-weight: 600;
}

.nav ul {
  display: flex;
  gap: 2rem;
  list-style: none;
  margin: 0;
  padding: 0;
}

.nav a {
  color: #2c3e50;
  text-decoration: none;
  font-weight: 500;
  transition: color 0.2s ease;
}

.nav a:hover {
  color: #42b983;
}
</style>
