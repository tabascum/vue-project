<script setup></script>

<template>
  <section class="home">
    <div>
      <figure>
        <img src="../assets/img/programmer-man.png" alt="" />
      </figure>
      <article>
        <h1>Vasco Marques</h1>
        <h2 id="position">FRONT END DEVELOPER</h2>
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

  .home figure {
    margin: 0;
    filter: drop-shadow(1rem 0.5rem 0.3rem #27363b);
  }

  .home figure img {
    width: 60%;
  }

  .home article {
    display: inherit;
    flex-direction: column;
    line-height: 0;
    align-items: end;
  }

  h1 {
    font-family: 'Bodoni Moda', serif;
  }

  h2 {
    color: #99b998;
  }
}
</style>
