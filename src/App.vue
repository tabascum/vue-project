<script setup>
import { RouterView } from 'vue-router'
import TopBarComponent from './components/TopBarComponent.vue'
import HeaderComponent from './components/HeaderComponent.vue'
import FooterComponent from './components/FooterComponent.vue'
</script>

<template>
  <TopBarComponent />
  <HeaderComponent />
  <RouterView />
  <FooterComponent />
</template>

<style scoped></style>
