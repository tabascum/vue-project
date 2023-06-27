<script setup>
import GithubIcon from '../components/icons/GithubIcon.vue'
</script>

<template>
  <div class="sections-wrapper">
    <section class="cards-wrapper">
      <h1>Projects</h1>
      <article class="cards">
        <figure>
          <img class="card" src="../assets/img/barber-page.png" alt="" />
          <figcaption>Barber Landing Page <GithubIcon /></figcaption>
        </figure>

        <figure>
          <img class="card" src="../assets/img/construction-page.png" alt="" />
          <figcaption>Construction Web Page <GithubIcon /></figcaption>
        </figure>

        <figure>
          <img class="card" src="../assets/img/api-consumption-page.png" alt="" />
          <figcaption>Weather App<GithubIcon /></figcaption>
        </figure>

        <figure>
          <img class="card" src="../assets/img/vue-notes-app.png" alt="" />
          <figcaption>Notes App<GithubIcon /></figcaption>
        </figure>

        <figure>
          <img class="card" src="../assets/img/restaurant-page.png" alt="" />
          <figcaption>Restaurant Page <GithubIcon /></figcaption>
        </figure>

        <figure>
          <img class="card" src="../assets/img/contact-form.png" alt="" />
          <figcaption>Page with contact form <GithubIcon /></figcaption>
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
  text-align: end;
}

.cards figure {
  cursor: pointer;
  transition: all 0.5s;
  text-align: end;
  transform: perspective(1000px) rotateY(-25deg);
}

.cards figure:hover {
  cursor: pointer;
  transform: none;
}

.cards figure img {
  width: 100%;
}

.cards figure img:hover {
  box-shadow: 0.3rem 0.3rem 0.8rem #489f9c;
}

figcaption {
  display: flex;
  justify-content: flex-end;
  align-items: center;
  gap: 0.5rem;
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

@media (max-width: 768px) {
  .cards {
    display: grid;
    grid-template-columns: repeat(1, 1fr);
  }
}
</style>
