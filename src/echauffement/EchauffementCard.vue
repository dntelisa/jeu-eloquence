<script setup lang="ts">
</script>

<template>
  <div class="echauffement-card">
    <h1>Echauffement</h1>
    <img src="../assets/images/echauffement.png" alt="Echauffement" />
    <p>Echauffe toi en répettant des phrases le plus rapidement possible.</p>
  </div>
</template>

<style scoped>
.echauffement-card {
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
