<template>
  <Navigation />
  <Header />
  <AboutUs />
  <Frameworks />
  <Faq />
  <Applications />
  <Footer />
</template>

<script>
import Header from '@/components/Header.vue';
import Navigation from '@/components/Navigation.vue';
import AboutUs from '@/components/AboutUs.vue';
import Frameworks from '@/components/Frameworks.vue';
import Faq from '@/components/Faq.vue';
import Applications from '@/components/Applications.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'App',
  components: {
    Header,
    Navigation,
    AboutUs,
    Frameworks,
    Faq,
    Applications,
    Footer,
},
}
</script>

<style>

</style>
