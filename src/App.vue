<script setup>
import { RouterView } from 'vue-router'
import TopBarComponent from './components/TopBarComponent.vue'
import HeaderComponent from './components/HeaderComponent.vue'
import FooterComponent from './components/FooterComponent.vue'
</script>

<template>
  <TopBarComponent />
  <main class="main">
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
