<script setup lang="ts">

</script>

<template>
  <div class="welcome-container">
    <p>Je suis un développeur web passionné</p>
    <p class="welcome-title">Développeur Full-Stack</p>
  </div>
</template>

<style scoped>
  .welcome-container {
    display: flex;
    flex-direction: column;
    text-align: left;
    padding: 150px 5%;
    height: calc(100vh - 100px);
  }

  .welcome-container p {
    font-size: 6rem;
    font-weight: 600;
    line-height: 1.2;
    color: #333;
  }

  .welcome-container .welcome-title {
    font-weight: 400;
    color: #767676;
  }
</style>