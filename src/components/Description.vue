<template>
  <div class="description">
    <p class="description__content">{{ content }}</p>
  </div>
</template>

<script setup>
const props = defineProps({
  content: String,
});
</script>

<style scoped>
.description {
  margin: 1rem 0;
}

.description__title {
  font-size: 1.25rem;
  font-weight: 600;
  margin-bottom: 0.5rem;
  color: #1a1a1a;
}

.description__content {
  font-size: 1rem;
  line-height: 1.5;
  color: #4a4a4a;
  display: -webkit-box;
}
</style>
