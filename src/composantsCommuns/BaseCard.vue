<script setup lang="ts">
defineProps<{
  title: string
  imgSrc: string
  description: string
}>()
</script>

<template>
  <div class="card" @click="$router.push('/' + title.toLowerCase().replace(' ', '-'))">
    <h1>{{ title }}</h1>
    <img :src="imgSrc" :alt="title" />
    <p>{{ description }}</p>
  </div>
</template>

<style scoped>
.card {
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color: #f0f0f0;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  width: 300px;
  margin: 20px;

  img {
    width: 100px;
    height: 100px;
    margin-bottom: 20px;
  }
}
</style>
