<template>
  <CustomHeader />
  <MainContent />
  <CustomFooter />
</template>

<script setup>
import CustomHeader from './components/CustomHeader.vue';
import CustomFooter from './components/CustomFooter.vue';
import MainContent from './components/MainContent.vue';
</script>

<style>
@import './assets/theme.css';

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

#app {
  min-height: 100vh;
  display: grid;
  grid-template-rows: min-content 1fr min-content;
  font-family: var(--font_sans);
  background: var(--bg0);
  color: var(--fg1);
}
</style>
