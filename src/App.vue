<script setup lang="ts"></script>

<template>
  <h1 @click="$router.push('/')">PALABRUME</h1>
  <router-view />
</template>

<style scoped>
h1 {
  display: flex;
  background-color: #42b983;
  justify-content: center;
  margin: 0;
  height: 100px;
  font-family: Arial, Helvetica, sans-serif;
  align-items: center;
}
</style>

<style>
html,
body {
  margin: 0;
  padding: 0;
}
</style>
