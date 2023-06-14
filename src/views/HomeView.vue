<script setup>
import { ref } from 'vue'
const code = '< FRONT END DEVELOPER />'
const typeValue = ref('')

const typeEffect = () => {
  if (typeValue.value.length < code.length) {
    typeValue.value += code.charAt(typeValue.value.length)
    setTimeout(typeEffect, 100)
  }
}
typeEffect()
</script>

<template>
  <section class="home">
    <div>
      <figure>
        <img src="../assets/img/programmer-man.png" alt="" />
      </figure>
      <article>
        <h1>Vasco Marques</h1>
        <span>
          <h2 class="typingEffect">{{ typeValue }}</h2>
        </span>
        <p>Welcome to my world!</p>
      </article>
      <article></article>
    </div>
  </section>
</template>

<style scoped>
@media (min-width: 1024px) {
  .home div {
    padding-inline: 1rem;
    display: flex;
    justify-content: space-around;
    align-items: center;
    text-align: center;
    line-height: 0;
    min-height: 80vh;
  }

  .home:nth-child(n) {
    font-size: 2.5rem;
    text-shadow: 0.2rem 0.2rem 0.2rem #27363b;
  }

  .home article {
    max-width: 50rem;
    display: inherit;
    flex-direction: column;
    line-height: 0;
    align-items: center;
    text-align: center;
    position: relative;
  }
}

.home figure {
  margin: 0;
  filter: drop-shadow(1rem 0.5rem 0.3rem #27363b);
}

.home figure img {
  width: 70%;
}

h1 {
  font-family: 'Bodoni Moda', serif;
}

h2 {
  font-size: 1.2em;
  color: #99b998;
}

@media (max-width: 1024px) {
  .home {
    display: inherit;
    justify-content: center;
    align-items: center;
    text-align: center;
  }

  .home figure {
    padding-block: 1rem;
  }
}
</style>
