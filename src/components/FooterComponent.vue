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
  line-height: 0;
  color: #489f9c;
  display: flex;
  align-items: end;
  justify-content: center;
  font-size: 1.2vw;
}

@media (max-width: 1024px) {
  footer {
    display: flex;
    justify-content: center;
    text-align: center;
  }
}
</style>
