<script setup>
// import HelloWorld from './components/HelloWorld.vue'
// import TheWelcome from './components/TheWelcome.vue'
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
  <!-- <header>
    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
      <HelloWorld msg="You did it!" />
    </div>
  </header> -->
  <Header />

  <main>
    <!-- <TheWelcome /> -->
     <div></div>
  </main>
</template>

<style scoped>
main>div {
  width: 100%;
  height: 1000px;
  background-color: var(--color-text);
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  mask-image: url(./assets/magicpattern-grid-pattern-1720454996065_4.svg);
  mask-size: auto 100%;
  mask-repeat: no-repeat;
}
/* header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
} */

@media (min-width: 1024px) {
  /* header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  } */
}
</style>
