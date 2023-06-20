<script setup>
import GithubIcon from '../components/icons/GithubIcon.vue'
</script>

<template>
  <div class="sections-wrapper">
    <section class="cards-wrapper">
      <h1>Projects</h1>
      <article class="cards">
        <figure>
          <img class="card" src="../assets/img/coding.jpg" alt="" />
          <figcaption>A small text</figcaption>
        </figure>

        <figure>
          <img class="card" src="../assets/img/coding.jpg" alt="" />
          <figcaption>A small text</figcaption>
        </figure>

        <figure>
          <img class="card" src="../assets/img/coding.jpg" alt="" />
          <figcaption>A small text <GithubIcon /></figcaption>
        </figure>

        <figure>
          <img class="card" src="../assets/img/coding.jpg" alt="" />
          <figcaption>A small text</figcaption>
        </figure>

        <figure>
          <img class="card" src="../assets/img/coding.jpg" alt="" />
          <figcaption>A small text</figcaption>
        </figure>
      </article>
    </section>
  </div>
</template>

<style>
.cards-wrapper {
  display: flex;
  justify-content: center;
  flex-direction: column;
}

.cards {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
}

.cards figure {
  cursor: pointer;
  transition: all 0.5s;
  text-align: end;
  transform: perspective(1000px) rotateY(-20deg);
}

.cards figure img:hover {
  cursor: pointer;
}

.cards figure img {
  width: 100%;
  box-shadow: 0.5rem 0.5rem 0.5rem #303844;
}

@media (max-width: 1024px) {
  .sections-wrapper {
    display: flex;
    flex-direction: column;
    text-align: center;
  }

  .cards-wrapper {
    min-height: 80vh;
    display: flex;
  }

  .cards {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
  }
}
</style>
