<script setup lang="ts">
const projects = [
  {
    title: 'Rocket Starflop',
    image: '/portfolio_v2/projects/rocket-starflop.png',
    description: 'Rocket Starflop est un jeu vidéo 3D développé en TypeScript avec le moteur de jeu Fibbo. Réalisé avec Augustin MERCIER à l\'occasion d\'un challenge de Benjamin Code.',
    technologies: ['TypeScript', 'Fibbo'],
    links: [
      {
        name: 'GitHub',
        url: 'https://github.com/Gugustinette/rocket-starflop'
      },
      {
        name: 'Jeu en ligne',
        url: 'https://gugustinette.github.io/rocket-starflop/'
      },
      {
        name: 'Vidéo',
        url: 'https://youtu.be/fxYmKtQgu7E?si=PROibbQNmKUgWZd4&t=507'
      }
    ]
  },
  {
    title: 'Mizuka',
    image: '/portfolio_v2/projects/mizuka.png',
    description: 'Mizuka est un bot Discord permettant la gestion d\'un serveur Discord de 60 000 membres anglophone et francophone. Il gère l\'expérience, des salons vocaux personnalisés, un shop, des commandes de modération et d\'autres. Gestion d\'un VPS pour le bot.',
    technologies: ['Java', 'MongoDB', 'JDA'],
    links: [
      {
        name: 'Discord',
        url: 'https://discord.gg/friends'
      }
    ]
  },
  {
    title: 'Chatting API',
    image: 'https://placehold.co/600x400/EEE/31343C',
    description: 'Chatting API est une API REST permettant de gérer des utilisateurs et des messages. Elle a été développée en PHP avec Laravel.',
    technologies: ['PHP', 'Laravel'],
  }
];
</script>

<template>
  <div class="project-container" id="projects-panel">
    <p class="project-title">Mes Projets</p>

    <div class="project-content">
      <div class="project-card" v-for="project in projects" :key="project.title">
        <p class="project-card-title">{{ project.title }}</p>
        <img alt="Image du projet" :src="project.image" class="project-card-image">
        <p class="project-card-description">{{ project.description }}</p>
        <div class="project-card-links">
          <a v-for="link in project.links" :key="link.name" :href="link.url" target="_blank">{{ link.name }}</a>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
  .project-container {
    display: flex;
    flex-direction: column;
    text-align: left;
    padding: 150px 5%;
    min-height: calc(100vh - 100px);
    background-color: #FBFBFB;
    gap: 100px;
  }

  .project-container .project-title {
    font-size: 3rem;
    font-weight: 600;
    line-height: 1.2;
    color: #333;
  }

  .project-content {
    display: flex;
    justify-content: space-between;
  }

  .project-card {
    width: 30%;
    padding: 20px;
    border-radius: 5px;
    background-color: #FFF;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  }

  .project-card-title {
    font-size: 1.5rem;
    font-weight: 600;
    color: #333;
    text-align: center;
  }

  .project-card-image {
    width: 100%;
    margin-top: 20px;
    height: 200px;
    object-fit: cover;
  }

  .project-card-description {
    font-size: 0.9rem;
    text-align: justify;
    color: #767676;
  }

  .project-card-links {
    display: flex;
    justify-content: space-around;
    margin-top: 20px;
  }

  .project-card-links a {
    text-decoration: none;
    color: #333;
    font-weight: 600;
    padding: 10px 20px;
    border-radius: 5px;
    transition: background-color 0.3s, color 0.3s;
  }

  .project-card-links a:hover {
    background-color: #F6F6F6;
    border-radius: 5px;
    color: #000;
  }

  @media (max-width: 850px) {
    .project-content {
      flex-direction: column;
    }

    .project-card {
      width: 100%;
      margin-top: 20px;
    }
  }

  @media (max-width: 480px) {
    .project-container {
      padding: 100px 5%;
    }

    .project-container .project-title {
      font-size: 2rem;
    }

    .project-card {
      padding: 10px;
    }

    .project-card-title {
      font-size: 1.2rem;
    }

    .project-card-description {
      font-size: 0.8rem;
    }
  }
</style>