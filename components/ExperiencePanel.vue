<script setup lang="ts">
const experiences = [
  {
    title: 'Développeur PHP/Full-Stack',
    date: '2024 - Aujourd\'hui',
    company: 'WeLogin',
    description: 'Développement des solutions et applications web de WeLogin à déstination des offices de tourisme français.',
    skills: ['PHP', 'Laravel', 'HTML', 'CSS', 'JavaScript', 'Git', 'JIRA', 'Confluence']
  },
  {
    title: 'Développeur Symfony/Angular alternant',
    date: '2022 - 2023',
    company: 'Dotnet SAS',
    description: 'Refonte du SaaS Fiche-paie.net avec Symfony et Angular (précédement fait en PHP Natif).',
    skills: ['Symfony', 'Angular', 'TypeScript', 'Figma', 'Git', 'JIRA', 'Confluence', 'Figma']
  },
  {
    title: 'Développeur WordPress stagiaire',
    date: '07/2022 - 09/2022',
    company: 'Dotnet SAS',
    description: 'Développement d\'un plugin pour la mise en vente de formation avec WooCommerce.',
    skills: ['WordPress', 'PHP', 'HTML', 'CSS', 'JavaScript', 'Git', 'Figma']
  }
];
</script>

<template>
  <div class="experience-container">
    <p class="experience-title">Mes Expériences</p>

    <div class="experience-content">
      <div class="experience-card" v-for="experience in experiences" :key="experience.title">
        <div class="experience-card-title-container">
          <p class="experience-card-title">{{ experience.title }}</p>
          <div class="experience-card-subtitle">
            <p>{{ experience.company }}</p>
            <p>{{ experience.date }}</p>
          </div>
        </div>
        <p class="experience-card-description">{{ experience.description }}</p>
        <div class="experience-card-skills">
          <span v-for="skill in experience.skills" :key="skill">{{ skill }}</span>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
  .experience-container {
    display: flex;
    flex-direction: column;
    text-align: left;
    padding: 150px 5%;
    height: calc(100vh);
    background-color: #FBFBFB;
    gap: 100px;
  }

  .experience-container .experience-title {
    font-size: 3rem;
    font-weight: 600;
    line-height: 1.2;
    color: #333;
  }

  .experience-card-title-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 10px;
  }

  /* Experience cards (one per line, joined by a black line in the middle) */
  .experience-content {
    display: flex;
    justify-content: space-between;
    flex-direction: column;
    gap: 20px;
    position: relative;
  }

  .experience-card {
    padding: 20px;
    border-radius: 5px;
    background-color: #FFF;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    z-index: 2;
  }

  .experience-card-title {
    font-size: 1.5rem;
    font-weight: 600;
    color: #333;
    text-align: center;
  }

  .experience-card-subtitle {
    display: flex;
    justify-content: center;
    gap: 20px;
    margin-top: 10px;
    color: #767676;
  }

  .experience-card-subtitle p {
    font-size: 0.9rem;
  }

  .experience-card-description {
    font-size: 0.9rem;
    text-align: justify;
    color: #767676;
  }

  .experience-card-skills {
    display: flex;
    justify-content: center;
    gap: 10px;
    margin-top: 20px;
  }

  .experience-card-skills span {
    padding: 3px 10px;
    border-radius: 15px;
    background-color: #A8A8A8;
    color: white;
    cursor: default;
    transition: background-color 0.3s;
  }

  .experience-card-skills span:hover {
    background-color: #9A9A9A;
  }

  .experience-content::before {
    content: '';
    position: absolute;
    top: -20px;
    bottom: 0;
    left: 50%;
    width: 5px;
    height: calc(100% + 40px);
    background-color: #000;
    z-index: 1;
  }

  .experience-content::after {
    content: '';
    position: absolute;
    top: -20px;
    left: 50%;
    border-left: 5px solid #000;
    border-top: 5px solid #000;
    width: 10px;
    height: 10px;
    z-index: 1;
    rotate: 45deg;
    translate: -34%;
  }

  /* Responsive design */
  @media (max-width: 768px) {
    .experience-container {
      flex-direction: column;
      height: auto;
    }

    .experience-content {
      flex-direction: column;
    }

    .experience-card {
      width: 100%;
      margin-bottom: 20px;
    }

    .experience-card + .experience-card {
      border-left: none;
      border-top: 1px solid #000;
    }
  }
</style>