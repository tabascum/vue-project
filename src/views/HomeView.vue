<script setup>
import { ref } from 'vue'
import SideStackComponent from '../components/SideStackComponent.vue'
const code = '< FRONT END DEVELOPER />'
const typeValue = ref('')

const typeEffect = () => {
  if (typeValue.value.length < code.length) {
    typeValue.value += code.charAt(typeValue.value.length)
    setTimeout(typeEffect, 100)
  }
}
typeEffect()

/*  */
</script>

<template>
  <section class="home">
    <!--     <figure>
      <img src="../assets/img/programmer-man.png" alt="" />
    </figure> -->
    <SideStackComponent />
    <article class="content-wrapper">
      <h1>Vasco Marques</h1>
      <span>
        <h2 class="typingEffect">{{ typeValue }}</h2>
      </span>
      <p>Welcome to my world!</p>
    </article>
  </section>
</template>

<style scoped>
@media (min-width: 1024px) {
  .home {
    display: flex;
    justify-content: space-evenly;
    align-items: center;
    text-align: center;
    line-height: 0;
    min-height: 80vh;
    font-size: 2rem;
  }

  .content-wrapper {
    display: inherit;
    flex-direction: column;
    justify-content: center;

    align-items: center;
    text-align: center;
    margin-inline: 1rem;
    width: 50%;
  }
}

.home figure {
  margin: 0;
  filter: drop-shadow(1rem 0.5rem 0.3rem #27363b);
}

.home figure img {
  width: 70%;
}

.content-wrapper:nth-child(n) {
  text-shadow: 0.2rem 0.2rem 0.2rem #27363b;
}

@media (max-width: 1024px) {
  .home {
    display: inherit;
    justify-content: center;
    align-items: center;
    text-align: center;
  }
  .home figure {
    padding-block: 2rem;
  }

  .content-wrapper:nth-child(n) {
    line-height: 1;
    text-shadow: 0.2rem 0.2rem 0.2rem #27363b;
  }
}
</style>
