<script setup>
import { RouterLink } from 'vue-router'
</script>

<template>
  <header>
    <div class="wrapper">
      <nav>
        <h1>&lt; VM/&gt;</h1>
        <span id="menu-wrapper">
          <div class="links-wrapper">
            <RouterLink class="link" to="/">HOME</RouterLink>
            <RouterLink class="link" to="/work">WORK</RouterLink>
            <RouterLink class="link" to="/contact">CONTACT</RouterLink>
          </div>

          <svg
            @click="prevent"
            id="menu"
            xmlns="http://www.w3.org/2000/svg"
            width="32"
            height="32"
            viewBox="0 0 24 24"
          >
            <path fill="currentColor" d="M3 18h18v-2H3v2zm0-5h18v-2H3v2zm0-7v2h18V6H3z" />
          </svg>
        </span>
      </nav>
    </div>
  </header>
</template>

<style scoped>
header {
  line-height: 0;
}

.wrapper nav,
#menu-wrapper {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

h1 {
  font-weight: 700;
  font-size: 2.5rem;
  padding-inline-end: 0.5rem;
}

.links-wrapper {
  gap: 1rem;
  display: flex;
  text-align: end;
}

.link {
  display: inline-block;
  position: relative;
  color: #489f9c;
  text-decoration: none;
  font-size: 1.2rem;
  padding-block: 1rem;
  transition: all 0.3s;
}

.link:hover {
  color: #66fcf1;
}

.link::after {
  content: '';
  position: absolute;
  width: 100%;
  transform: scaleX(0);
  height: 0.1rem;
  bottom: 0;
  left: 0;
  background-color: #66fcf1;
  transform-origin: bottom right;
  transition: transform 0.25s ease-out;
}

.link:hover::after {
  transform: scaleX(1);
  transform-origin: bottom left;
}

#menu {
  display: none;
  cursor: pointer;
}

@media (max-width: 600px) {
  .wrapper nav {
    padding-inline: 0.5rem;
  }
  .links-wrapper {
    display: none;
    line-height: 0.5;
    flex-direction: column;
    align-items: flex-end;
  }

  #menu {
    display: inline;
  }
}
</style>
