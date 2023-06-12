<script setup>
import { RouterView } from 'vue-router'
import HeaderComponent from './components/HeaderComponent.vue'
import FooterComponent from './components/FooterComponent.vue'
import TopBarComponent from './components/TopBarComponent.vue'
</script>

<template>
  <TopBarComponent />
  <main class="main">
    <HeaderComponent class="header" />
    <RouterView />
    <FooterComponent />
  </main>
</template>

<style scoped></style>
