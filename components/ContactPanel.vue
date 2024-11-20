<script setup lang="ts">
const contacts = [
  {
    icon: 'uil:linkedin',
    link: 'https://www.linkedin.com/in/mael-caubere/'
  },
  {
    icon: 'uil:github',
    link: 'https://www.github.com/oulahoop',
  },
  {
    icon: 'uil:envelope',
    link: 'mailto:maelcaubere@live.fr'
  },
  {
    icon: 'uil:twitter',
    link: 'https://x.com/KCZyraa'
  }
];

</script>

<template>
  <div class="contact-container" id="contact-panel">
    <p class="contact-title">Contact</p>

    <div class="icons-container">
      <a v-for="contact in contacts" :key="contact.icon" :href="contact.link" target="_blank">
        <Icon :name="contact.icon" size="50" class="contact-icon"/>
      </a>
    </div>
  </div>
</template>

<style scoped>
  .contact-container {
    display: flex;
    flex-direction: column;
    text-align: left;
    padding: 150px 5%;
    margin-bottom: 100px;
    background-color: #fff;
    gap: 100px;
  }

  .contact-container .contact-title {
    font-size: 3rem;
    font-weight: 600;
    line-height: 1.2;
    color: #333;
  }

  .icons-container {
    display: flex;
    justify-content: center;
    gap: 40px;
  }

  .contact-icon {
    color: #555;
    cursor: pointer;
    transition: all 0.3s;
  }

  .contact-icon:hover {
    color: #222;
    scale: 1.1;
  }
</style>