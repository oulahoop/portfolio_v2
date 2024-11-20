<script setup lang="ts">

</script>

<template>
  <div class="header-container">
    <div class="header-left-content">
      <a href="#welcome-panel" class="header-title">Maël Caubere</a>
    </div>

    <div class="header-right-content">
      <ul class="header-menu">
        <li>
          <a href="#projects-panel">Projets</a>
        </li>
        <li>
          <a href="#experiences-panel">Expériences</a>
        </li>
        <!--<li>
          <a href="#skills-panel">Compétences</a>
        </li>
        <li>
          <a href="#formation-panel">Formations</a>
        </li>-->
        <li>
          <a href="#contact-panel">Contact</a>
        </li>
      </ul>
    </div>
  </div>
</template>

<style scoped>
  .header-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 20px;
    height: 100px;
    position: sticky;
    top: 0;
    background-color: #F9F9F9;
    z-index: 10;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  }

  .header-left-content {
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .header-right-content {
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .header-title {
    font-size: 1.5rem;
    font-weight: bold;
    text-decoration: none;
    color: black;
  }

  .header-menu {
    display: flex;
    list-style: none;
  }

  .header-menu li {
    margin: 0 10px;
  }

  .header-menu a {
    text-decoration: none;
    color: black;
  }

  .header-menu a:hover {
    color: blue;
  }

  @media (max-width: 768px) {
    .header-container {
      padding: 0 10px;
    }

    .header-title {
      font-size: 1.2rem;
    }

    .header-menu li {
      margin: 0 5px;
    }
  }

  @media (max-width: 480px) {
    .header-menu {
      display: none;
    }

    .header-right-content {
      display: none;
    }

    .header-container {
      justify-content: center;
    }
  }
</style>