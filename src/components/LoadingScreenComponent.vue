<script setup>
import { reactive } from 'vue'

const content = reactive({ info: {} })

/* onMounted(async () => {
  const data = await new Promise((resolve) => {
    setTimeout(() => {
      resolve({
        intro1: 'Not that long time ago...',
        intro2: 'In a country, not that far away...',
        title: 'Vasco M.',
        description: `Lorem ipsum dolor, sit amet consectetur adipisicing elit. Provident eligendi accusantium,
          aut sunt eius quisquam? Eius explicabo tenetur quisquam voluptatem exercitationem
          praesentium unde tempore consequuntur non! Sapiente eaque aut, fuga placeat hic aliquam
          nostrum non ex. Dolore unde quibusdam eius error saepe autem, ratione expedita sit
          dolorem, hic distinctio minima? Lorem ipsum dolor sit amet consectetur adipisicing elit.
          Voluptatibus dolor, dolorum assumenda maiores voluptas, natus fugiat ullam quae expedita
          ratione reiciendis blanditiis consectetur libero mollitia amet eius sint, quaerat
          exercitationem.`
      })
    }, 200)
  })
  content.info = data
}) */

async function getLoader() {
  return await new Promise((resolve) => {
    setTimeout(() => {
      resolve({
        intro: 'Not that long time ago...", "In a country, not that far away...',
        title: 'Vasco M.',
        description: `Lorem ipsum dolor, sit amet consectetur adipisicing elit. Provident eligendi accusantium,
          aut sunt eius quisquam? Eius explicabo tenetur quisquam voluptatem exercitationem
          praesentium unde tempore consequuntur non! Sapiente eaque aut, fuga placeat hic aliquam
          nostrum non ex. Dolore unde quibusdam eius error saepe autem, ratione expedita sit
          dolorem, hic distinctio minima? Lorem ipsum dolor sit amet consectetur adipisicing elit.
          Voluptatibus dolor, dolorum assumenda maiores voluptas, natus fugiat ullam quae expedita
          ratione reiciendis blanditiis consectetur libero mollitia amet eius sint, quaerat
          exercitationem.`
      })
    }, 2000)
  })
}

content.info = await getLoader()
</script>

<template>
  <audio autoplay>
    <source src="../assets/sound/cinematic-trailer-music.mp3" type="audio/mp3" />
  </audio>
  <section class="section">
    <article class="intro">{{ content.info.intro1 }} <br />{{ content.info.intro2 }}</article>
    <div class="content-wrapper">
      <article class="loading-content">
        <h1>{{ content.info.title }}</h1>
        <p>
          {{ content.info.description }}
        </p>
      </article>
    </div>
  </section>
</template>

<style scoped>
.intro {
  position: absolute;
  top: 30%;
  left: 25%;
  z-index: 1;
  animation: intro 6s ease-out 1s;
  color: #99b998;
  font-weight: 400;
  font-size: 250%;
  opacity: 0;
}

@keyframes intro {
  0% {
    opacity: 0;
  }
  20% {
    opacity: 1;
  }
  90% {
    opacity: 1;
  }
  100% {
    opacity: 0;
  }
}

.content-wrapper {
  transform: perspective(300px) rotateX(20deg);
  text-shadow: 0.2rem 0.2rem 0.2rem #27363b;
  transform-origin: 50% 100%;
  text-align: justify;
  position: absolute;
  margin-left: -9em;
  font-weight: bold;
  overflow: hidden;
  font-size: 350%;
  height: 50em;
  width: 18em;
  bottom: 0;
  left: 50%;
}

.content-wrapper:after {
  position: absolute;
  content: ' ';
  bottom: 60%;
  left: 0;
  right: 0;
  top: 0;
}

.loading-content {
  animation: scroll 100s linear 10s;
  position: absolute;
  top: 100%;
}

@keyframes scroll {
  0% {
    top: 100%;
  }
  100% {
    top: -170%;
  }
}

.loading-content h1 {
  text-align: center;
}
</style>
