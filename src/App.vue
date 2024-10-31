<script setup>
import Header from "./components/Header.vue"
import Presentation from "./components/Presentation.vue"
import Experience from "./components/Experience.vue"
import { onMounted, ref, computed } from "vue";

// const storageTheme = localStorage.getItem('theme');
// const systemColorScheme = window.matchMedia('(prefers-color-scheme: dark)').matches ? 'dark' : 'light';

// const newTheme = storageTheme ?? systemColorScheme;

// document.documentElement.setAttribute('data-theme', newTheme);

const URL_SEARCHPARAMS = new URLSearchParams(window.location.search);
const USER_LANGUAGE = String(navigator.language || navigator.userLanguage).split("-")[0];
if (URL_SEARCHPARAMS.get("lang") !== "en") {
  URL_SEARCHPARAMS.set("lang","en");
  window.location.search = URL_SEARCHPARAMS;
}

onMounted(() => {
  
})
</script>

<template>
  <Header />

  <main>
    <div class="background"></div>
    <Presentation id="home" />
    <Experience id="experience" />
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
  scroll-padding-top: 40px;
  gap: 60px;
  scroll-snap-type: y proximity;
}
main > div.background {
  position: absolute;
  z-index: 1;
  width: 100%;
  height: -webkit-fill-available;
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
