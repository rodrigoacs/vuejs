<template>
  <div>
    <h2>{{ $t("projects.title") }}</h2>
    <div class="projects-wrapper">
      <a
        href="https://time.rodrigoacs.com/"
        target="_blank"
      >
        <img
          class="project-card"
          alt="time-tracker"
          src=""
        />
      </a>
      <a
        href="https://git-aesthetics.rodrigoacs.com/"
        target="_blank"
      >
        <img
          class="project-card"
          alt="git-aesthetics"
          src=""
        />
      </a>
    </div>
  </div>
</template>

<script setup>
import { onMounted } from 'vue'
import { generateGithubStatsUrl } from '../githubCard.js'

onMounted(() => {
  defaultProjectTheme()
})

function defaultProjectTheme() {
  const projectsCards = document.querySelectorAll('.project-card')
  projectsCards.forEach(card => {
    if (document.documentElement.classList.contains('dark')) {
      card.src = generateGithubStatsUrl(card.alt, 'dark')
    } else {
      card.src = generateGithubStatsUrl(card.alt, 'light')
    }
  })
}
</script>

<style scoped>
.projects-wrapper {
  display: flex;
  gap: 1.6rem;
  justify-content: center;
}

img {
  width: auto;
  height: 120px;
}

h2 {
  margin-top: 1.6rem;
  margin-bottom: 0.8rem;
}

p {
  margin-bottom: 0.8rem;
}
</style>
