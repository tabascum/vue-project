<script setup></script>

<template>
  <section class="home">
    <figure>
      <img src="../assets/img/programmer-man.png" alt="" />
    </figure>
    <article>
      <h1>Vasco Marques</h1>
      <h2>Frontend Developer</h2>
      <p>Welcome to my world!</p>
    </article>
  </section>
</template>

<style scoped>
@media (min-width: 1024px) {
  .home {
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

  .home figure {
    filter: drop-shadow(1rem 0.5rem 0.3rem #27363b);
  }

  .home article {
    font-family: 'Bodoni Moda', serif;
    display: inherit;
    flex-direction: column;
    line-height: 0;
  }
}
</style>
