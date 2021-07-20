<template>
  <div>
    <FooterTop/>
    <FooterBottom/>

    <!-- copyright -->
    <section class="copy">
      <div>Copyright Boolean &reg;</div>
    </section>
    <!-- end copyright -->

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
@import '../style/common.scss';

.copy{
  background-color: $m_orange;
  color: white;
  text-align: center;
  
  div{
    padding: 0.75rem;
    font-size: $fSize_7;
  }
}

</style>
