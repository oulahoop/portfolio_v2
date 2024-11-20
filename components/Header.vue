<script setup lang="ts">

</script>

<template>
  <div class="header-container">
    <div class="header-left-content">
      <p class="header-title">Maël Caubere</p>
    </div>

    <div class="header-right-content">
      <ul class="header-menu">
        <li>
          <a href="#">Projets</a>
        </li>
        <li>
          <a href="#">Expériences</a>
        </li>
        <li>
          <a href="#">Compétences</a>
        </li>
        <li>
          <a href="#">Formations</a>
        </li>
        <li>
          <a href="#">Contact</a>
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
      flex-direction: column;
      height: auto;
    }

    .header-right-content {
      margin-top: 20px;
    }
  }

  @media (max-width: 480px) {
    .header-menu {
      flex-direction: column;
    }

    .header-menu li {
      margin: 10px 0;
    }
  }
</style>