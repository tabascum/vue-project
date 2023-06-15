<script setup>
let currentYear = document.getElementById('#currentYear')
</script>

<template>
  <footer>
    <div class="footer-wrapper">
      <p>
        Conceived and Developed by Vasco Marques &copy;
        <span id="currentYear">{{ (currentYear = new Date().getFullYear()) }}</span> All rights
        reserved
      </p>
    </div>
  </footer>
</template>

<style scoped>
footer {
  color: #99b998;
  display: flex;
  align-items: end;
  justify-content: center;
  font-size: 1vw;
}

@media (max-width: 1024px) {
  footer {
    color: #99b998;
    display: flex;
    justify-content: center;
    text-align: center;
  }
}
</style>
