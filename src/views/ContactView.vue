<script setup></script>

<template>
  <section class="contact">
    <div>
      <form action="#">
        <div>
          <input type="text" />
          <label for="name">name</label>
        </div>
        <div>
          <input type="tel" />
          <label for="name">phone</label>
        </div>
        <div>
          <input type="email" />
          <label for="name">email</label>
        </div>
        <div>
          <textarea name="" id="" cols="20" rows="10"></textarea>
          <label for="textarea">message</label>
        </div>
        <button>send</button>
      </form>
    </div>
  </section>
</template>

<style scoped>
@media (min-width: 1024px) {
  .contact {
    min-height: 100vh;
    display: flex;
  }
}

form,
div {
  display: flex;
  flex-direction: column;
}

[input],
[textarea] {
  outline: none;
}
</style>
