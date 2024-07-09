<script setup>
import Header from "./components/Header.vue"
import Presentation from "./components/Presentation.vue"
import { onMounted, ref, computed } from "vue";

const storageTheme = localStorage.getItem('theme');
const systemColorScheme = window.matchMedia('(prefers-color-scheme: dark)').matches ? 'dark' : 'light';

const newTheme = storageTheme ?? systemColorScheme;

document.documentElement.setAttribute('data-theme', newTheme);

onMounted(() => {
  // const switcherTheme = document.querySelector('.main__check');
  // const root = document.documentElement;

  // if(root.getAttribute('data-theme') === 'dark'){
  //   switcherTheme.checked = true;      
  // } 

  // function toggleTheme(){
      
  //     const setTheme = this.checked ? 'dark' : 'light';
  //     root.setAttribute('data-theme', setTheme);
  
  //     localStorage.setItem('theme', setTheme);
  // }
  

  // switcherTheme.addEventListener('click', toggleTheme);
})
</script>

<template>
  <Header />

  <main>
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
}

@media (min-width: 1024px) {

}
</style>
