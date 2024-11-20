<template>
  <Header></Header>
  <WelcomePanel></WelcomePanel>
  <ProjectPanel></ProjectPanel>
  <ExperiencePanel></ExperiencePanel>
  <ContactPanel></ContactPanel>
  <Footer></Footer>
</template>

<style>
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    scroll-behavior: smooth;
  }

  body {
    font-family: 'Roboto', sans-serif;
  }

  h1 {
    font-size: 2rem;
  }

  p {
    font-size: 1rem;
  }
</style>
<script setup lang="ts">
import WelcomePanel from "~/components/WelcomePanel.vue";
</script>