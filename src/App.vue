<script setup>
import { RouterView } from 'vue-router'
import TopBarComponent from './components/TopBarComponent.vue'
import HeaderComponent from './components/HeaderComponent.vue'
import FooterComponent from './components/FooterComponent.vue'
import LoadingScreenComponent from './components/LoadingScreenComponent.vue'
</script>

<template>
  <LoadingScreenComponent />
  <TopBarComponent />
  <main class="main">
    <HeaderComponent />
    <RouterView />
  </main>
  <FooterComponent />
</template>

<style scoped></style>
