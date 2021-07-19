<template>
  <div>
    <FooterTop/>
    <FooterBottom/>
  </div>
</template>

<script>
import FooterTop from './FooterTop.vue'
import FooterBottom from './FooterBottom.vue'

export default {
  name: 'Footer',
  components:{
    FooterTop,
    FooterBottom,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
