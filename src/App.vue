<template>
  <div id="app">
    
    <div class="arrowUp shadow">
      <a href="#">
        <i class="bi bi-arrow-up"></i>
      </a>
    </div>

    <Header/>
    <Main/>
    <Footer/>
    
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
}
</script>

<style lang="scss">
@import '@/style/general.scss';
@import '@/style/common.scss';

#app {
  font-family: Source Sans Pro, Libre Baskerville, sans-serif;
}

.arrowUp{
  z-index: 2;
  position: fixed;
  background-color: white;
  width: 50px;
  height: 50px;
  position: fixed;
  bottom: 20px;
  right: 20px;
  border-radius: 50%;
  
  i{
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    font-size: 2rem;
    color: $m_orange;
  }
}

</style>
