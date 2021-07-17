<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <Header/>
    <Main/>
    <Footer msg="Welcome to Your Footer"/>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Main from './components/Main.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer,
  },

  data() {
    return {
      
    }
  },



}
</script>

<style lang="scss">
@import '@/style/general.scss';
@import '@/style/common.scss';

#app {
  font-family: Source Sans Pro, Libre Baskerville, sans-serif;
}

</style>
