<template>
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <Navigation />
  <Header />
  <AboutUs />
  <Frameworks />
  <Faq />
  <Applications />
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue';
import Header from '@/components/Header.vue';
import Navigation from '@/components/Navigation.vue';
import AboutUs from '@/components/AboutUs.vue';
import Frameworks from '@/components/Frameworks.vue';
import Faq from '@/components/Faq.vue';
import Applications from '@/components/Applications.vue';

export default {
  name: 'App',
  components: {
    // HelloWorld,
    Header,
    Navigation,
    AboutUs,
    Frameworks,
    Faq,
    Applications,
},
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Gothic+A1:wght@400;700&family=Roboto&display=swap');

*,
*::before,
*::after {
  box-sizing: border-box;
}

body,
h1,
h2,
h3,
h4,
p,
ul[class],
ol[class],
li,
figure,
figcaption,
blockquote,
dl,
dd {
  margin: 0;
}

#app {
  height: 100vh;
  scroll-behavior: smooth;
  text-rendering: optimizeSpeed;
  line-height: 26px;
  background-color: #F5F7FA;
  font-family: GothicA1, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #3D3D3D;
}

.container {
  height: 100%;
  margin: 0 auto;
}

.btn {
  width: 240px;
  height: 40px;
}
</style>
