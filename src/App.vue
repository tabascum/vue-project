<script setup>
import { RouterView } from 'vue-router'
import TopBarComponent from './components/TopBarComponent.vue'
import HeaderComponent from './components/HeaderComponent.vue'
import FooterComponent from './components/FooterComponent.vue'
import { ref } from 'vue'
import LoadingScreenComponent from './components/LoadingScreenComponent.vue'

const view = ref(true)
</script>

<template>
  <Suspense>
    <template #default>
      <main class="main">
        <TopBarComponent />
        <main>
          <HeaderComponent />
          <RouterView />
        </main>
        <FooterComponent />
      </main>
    </template>
    <template #fallback>
      <component :is="view ? LoadingScreenComponent : ''"></component>
    </template>
  </Suspense>
</template>

<style scoped>
.main {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
</style>
