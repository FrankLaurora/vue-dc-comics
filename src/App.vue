<template>
  <div id="app">
    <Header/>
    <Main/>
    <Shop/>
    <Footer/>
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Main from './components/Main.vue';
import Shop from './components/Shop.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Shop,
    Footer
  }
}
</script>

<style lang="scss">
  @import './assets/style/common.scss';
</style>
