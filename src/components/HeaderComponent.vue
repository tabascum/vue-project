<script setup>
import { RouterLink } from 'vue-router'
</script>

<template>
  <header>
    <div class="wrapper">
      <nav>
        <h1>VM.</h1>
        <div class="links-wrapper">
          <RouterLink class="link" to="/">HOME</RouterLink>
          <RouterLink class="link" to="/about">WORK</RouterLink>
          <RouterLink class="link" to="/contact">CONTACT</RouterLink>
          <!--           <span>
            <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24">
              <path fill="currentColor" d="M3 18h18v-2H3v2zm0-5h18v-2H3v2zm0-7v2h18V6H3z" />
            </svg>
          </span> -->
        </div>
      </nav>
    </div>
  </header>
</template>

<style scoped>
header {
  border-radius: 0.8rem;
  background: #2a363b;
  box-shadow: 0.5rem 0.5rem 1rem rgba(0, 0, 0, 0.5);
}

.wrapper {
  padding-inline: 1rem;
}

.wrapper nav,
.links-wrapper {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 0.8rem;
}

.wrapper nav h1 {
  font-family: 'Bodoni Moda', serif;
  font-weight: 500;
  font-size: 2.5rem;
}

.link {
  display: inline-block;
  position: relative;
  color: #f4837d;
  text-decoration: none;
  font-size: 1.2rem;
  padding-inline: 0.2rem;
  transition: all 0.3s;
}

.link::after {
  content: '';
  position: absolute;
  width: 100%;
  transform: scaleX(0);
  height: 2px;
  bottom: 0;
  left: 0;
  background-color: #99b898;
  transform-origin: bottom right;
  transition: transform 0.25s ease-out;
}

.link:hover::after {
  transform: scaleX(1);
  transform-origin: bottom left;
}
</style>
