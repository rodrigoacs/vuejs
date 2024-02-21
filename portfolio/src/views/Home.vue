<template>
  <Bio />
  <Projects />
</template>

<script setup>
import Bio from '@/components/Bio.vue'
import Projects from '@/components/Projects.vue'
import { onMounted } from 'vue'
import { generateGithubStatsUrl } from '../githubCard.js'

onMounted(() => {
  changeProjectCardTheme()
})

function changeProjectCardTheme() {
  console.log('changeProjectCardTheme')
  const projectsCards = document.querySelectorAll('.project-card')
  console.log(projectsCards)
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
h2 {
  margin-bottom: 0.8rem;
}

p {
  margin-bottom: 0.8rem;
}
</style>
