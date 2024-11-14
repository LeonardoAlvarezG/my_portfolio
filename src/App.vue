<script setup>
import Header from "./components/Header.vue"
import Presentation from "./components/Presentation.vue"
import Projects from "./components/Projects.vue";
import Experience from "./components/Experience.vue"
import CallToAction from "./components/CallToAction.vue";
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
    <Presentation id="home" />
    <Projects id="projects" />
    <CallToAction />
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
  /* padding-top: 40px; */
  scroll-padding-top: 40px;
  gap: 60px;
  scroll-snap-type: y proximity;
}

@media (min-width: 1024px) {

}
</style>
