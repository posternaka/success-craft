<template>
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <Navigation />
  <Header />
  <AboutUs />
  <Frameworks />
  <Faq />
  <Applications />
  <ContactUs />
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue';
import Header from '@/components/Header.vue';
import Navigation from '@/components/Navigation.vue';
import AboutUs from '@/components/AboutUs.vue';
import Frameworks from '@/components/Frameworks.vue';
import Faq from '@/components/Faq.vue';
import Applications from '@/components/Applications.vue';
import ContactUs from './components/ContactUs.vue';

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
    ContactUs,
},
}
</script>

<style>
/* Указываем box sizing */
*,
*::before,
*::after {
  box-sizing: border-box;
}

/* Убираем внутренние отступы */
ul[class],
ol[class] {
  padding: 0;
}

/* Убираем внешние отступы */
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

/* Выставляем основные настройки по-умолчанию для body */
body {
  
}

/* Удаляем стандартную стилизацию для всех ul и il, у которых есть атрибут class*/
ul[class],
ol[class] {
  list-style: none;
}

/* Элементы a, у которых нет класса, сбрасываем до дефолтных стилей */
a:not([class]) {
  text-decoration-skip-ink: auto;
}

/* Упрощаем работу с изображениями */
img {
  max-width: 100%;
  display: block;
}

/* Указываем понятную периодичность в потоке данных у article*/
article > * + * {
  margin-top: 1em;
}

/* Наследуем шрифты для инпутов и кнопок */
input,
button,
textarea,
select {
  font: inherit;
}

/* Удаляем все анимации и переходы для людей, которые предпочитай их не использовать */
@media (prefers-reduced-motion: reduce) {
  * {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
    scroll-behavior: auto !important;
  }
}

@font-face {
  font-family: 'GothicA1';
  src: local('GothicA1'),
    url('~@/assets/fonts/GothicA1-Regular.ttf') format('ttf');
  font-style: normal;
}



#app {
  height: 100vh;
  scroll-behavior: smooth;
  text-rendering: optimizeSpeed;
  line-height: 26px;
  background-color: #F5F7FA;
  /* height: 100%;        */
  font-family: GothicA1, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #3D3D3D;
}

.container {
  width: 1196px;
  height: 100%;
  margin: 0 auto;
}
</style>
