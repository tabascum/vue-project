<script setup>
import { RouterView } from 'vue-router'
import TopBarComponent from './components/TopBarComponent.vue'
import HeaderComponent from './components/HeaderComponent.vue'
import FooterComponent from './components/FooterComponent.vue'
import LoadingScreenComponent from './components/LoadingScreenComponent.vue'

const LoadingScreen = LoadingScreenComponent

window.addEventListener('DOMContentLoaded', () => {
  setTimeout(() => {
    LoadingScreen
  }, 10000)
})
</script>

<template>
  <TopBarComponent />
  <main class="main">
    <LoadingScreenComponent />
    <HeaderComponent class="header" />
    <RouterView />
  </main>
  <FooterComponent />
</template>

<style scoped>
.main {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
</style>
