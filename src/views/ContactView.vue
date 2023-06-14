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
    align-items: center;
    justify-content: end;
    margin-inline-end: 3rem;
  }
}

form,
div {
  display: flex;
  flex-direction: column;
}

form {
  width: 100%;
  padding: 1rem;
  border-radius: 0.5rem 0;
  background: linear-gradient(40deg, #f4837d 10%, #eb4960 100%);
}

[input],
[textarea] {
  outline: none;
}
</style>
