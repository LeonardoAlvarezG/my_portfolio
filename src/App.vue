<script setup>
import Header from "./components/Header.vue"
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

  <main></main>
</template>

<style scoped>
main {
  width: 100%;
  height: 1000px;
  background-color: var(--vt-c-black-mute);
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  mask-image: url(./assets/magicpattern-grid-pattern-1720454996065_4.svg);
  mask-size: auto 100%;
  mask-repeat: no-repeat;
}

@media (min-width: 1024px) {

}
</style>
