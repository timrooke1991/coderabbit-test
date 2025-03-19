<script setup>
defineProps<Props>();
</script>

<template>
  <ul>
    <li v-for="item in items" :key="item">{{ item }}</li>
  </ul>
</template>

<style>
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
