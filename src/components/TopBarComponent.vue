<script setup>
import GithubIcon from './icons/GithubIcon.vue'
import LinkedInIcon from './icons/LinkedInIcon.vue'
import LangToggleIcon from './icons/LangToggleIcon.vue'

let gitHubLink = 'https://github.com/tabascum'
let linkedInLink = 'https://www.linkedin.com/in/vascodmarques/'
</script>

<template>
  <section class="top-bar">
    <a :href="gitHubLink" target="_blank"><GithubIcon /></a>
    <a :href="linkedInLink" target="_blank"><LinkedInIcon /></a>
    <a href=""><LangToggleIcon /></a>
  </section>
</template>

<style scoped>
.top-bar {
  display: flex;
  justify-content: end;
  font-size: 1rem;
  gap: 1rem;
}

.top-bar a {
  color: #66fcf1;
  transition: all 0.8s;
}

.top-bar a:hover {
  color: #489f9c;
}
</style>
