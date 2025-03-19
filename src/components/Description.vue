<template>
  <div class="description">
    <h3 v-if="title" class="description__title">{{ title }}</h3>
    <p class="description__content" :style="{ '-webkit-line-clamp': maxLines }">
      {{ content }}
    </p>
  </div>
</template>

<script setup lang="ts">
interface Props {
  title?: string;
  content: string;
  maxLines?: number;
}

const props = withDefaults(defineProps<Props>(), {
  title: "",
  maxLines: 3,
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
  -webkit-box-orient: vertical;
  overflow: hidden;
  text-overflow: ellipsis;
}
</style>
