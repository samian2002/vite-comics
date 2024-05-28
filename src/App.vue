<template>
  <div id="app">
    <AppHeader />
    <MainContent />
    <Footer />
  </div>
</template>

<script>
import AppHeader from './components/Header.vue';
import MainContent from './components/MainContent.vue';
import Footer from './components/Footer.vue';

export default {
  components: {
    AppHeader,
    MainContent,
    Footer
  }
}
</script>

<style>
#app {
  font-family: Arial, sans-serif;
}
</style>
