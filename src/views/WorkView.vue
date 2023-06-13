<script setup></script>

<template>
  <h1>Projects</h1>
  <section class="work">
    <article class="cards">
      <figure>
        <img class="card-0" src="../assets/img/coding.jpg" alt="" />
        <figcaption>A small text</figcaption>
      </figure>
      <figure>
        <img class="card-1" src="../assets/img/coding.jpg" alt="" />
        <figcaption>A small text</figcaption>
      </figure>
      <figure>
        <img class="card-2" src="../assets/img/coding.jpg" alt="" />
        <figcaption>A small text</figcaption>
      </figure>
    </article>
  </section>
</template>

<style>
.cards {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-rows: 1fr 1fr 1fr;
  gap: 0px 0px;
  grid-template-areas:
    'card-0 card-0 .'
    '. card-1 card-1'
    'card-2 card-2 .';
}

.card-0 {
  grid-area: card-0;
}
.card-1 {
  grid-area: card-1;
}
.card-2 {
  grid-area: card-2;
}

.cards figure img {
  width: 50%;
}

@media (min-width: 1024px) {
  .work {
    min-height: 100vh;
    display: flex;
  }
}
</style>
