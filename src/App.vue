<script setup>
import Header from "./components/Header.vue"
import Presentation from "./components/Presentation.vue"
import { onMounted, ref, computed } from "vue";

const storageTheme = localStorage.getItem('theme');
const systemColorScheme = window.matchMedia('(prefers-color-scheme: dark)').matches ? 'dark' : 'light';

const newTheme = storageTheme ?? systemColorScheme;

document.documentElement.setAttribute('data-theme', newTheme);

onMounted(() => {
  
})
</script>

<template>
  <Header />

  <main id="home">
    <div class="background"></div>
    <Presentation />
  </main>
</template>

<style scoped>
main {
  display: flex;
  flex-direction: column;
  align-items: center;
  position: relative;
  width: 100%;
  height: fit-content;
  padding-top: 40px;
  scroll-snap-type: proximity;
}
main > div.background {
  position: absolute;
  z-index: 1;
  width: 100%;
  height: 400px;
  background-color: var(--color-background-soft);
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  mask-image: url(./assets/background_pattern.svg);
  mask-size: cover;
  mask-repeat: no-repeat;
  mask-position: top center;
  transition: all ease 0.5s;
}

@media (min-width: 1024px) {

}
</style>
