<script setup></script>

<template>
  <section>
    <h1>My Stack</h1>
  </section>
  <section class="work">
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
        <figcaption>A small text</figcaption>
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
</template>

<style>
section {
  display: flex;
}
.work {
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.cards {
  display: flex;
}

.cards figure img {
  width: 100%;
}

@media (min-width: 1024px) {
  .work {
    min-height: 80vh;
    display: flex;
  }
}
</style>
