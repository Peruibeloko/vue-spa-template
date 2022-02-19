<template>
  <footer>
    <section class="links">
      <ul>
        <li v-for="link in links" :key="link.href">
          <a :href="link.href">{{ link.text }}</a>
        </li>
      </ul>
    </section>
    <section class="footnote">
      <small>Oh look, its a footnote!</small>
    </section>
  </footer>
</template>

<script setup>
const links = [
  {
    href: 'https://github.com/peruibeloko/vue-spa-template',
    text: 'Check the source here!'
  },
  {
    href: 'https://github.com/peruibeloko',
    text: 'Check my other projects here!'
  }
];
</script>

<style scoped>
@import '../assets/theme.css';

ul {
  list-style: none;
  display: flex;
}

li::after {
  content: '·';
  padding: 0 1rem;
}

li:last-child::after {
  content: none;
}

li a {
  text-decoration: none;
  color: var(--bright_yellow);
}

footer {
  padding: 1rem 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

section {
  padding: 0.5rem 0;
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
