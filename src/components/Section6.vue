<template>
  <div class="bg_dark">
    <div class="bg_title">Testimonials.</div>

    <div class="content debug">

      <div class="left">
        <i class="bi bi-arrow-left"></i>
      </div>

      <!-- center -->
      <div class="center" v-for="(item, i) in Sec6" :key="i">
        <div class="image">
          <img :src="item.url" alt="">
        </div>
        <div class="name"></div>
        <div class="text"></div>
        <div class="scrollbar"></div>
      </div>
      <!-- end center -->

      <div class="right">
        <i class="bi bi-arrow-right"></i>
      </div>

    </div>
  </div>


</template>

<script>

import Sec6 from "@/data/Sec6.js"
export default {
  name: 'Section6',
  data() {
    return {
      Sec6
    }
  },
}
</script>

<style lang="scss" scoped>
@import '../style/common.scss';

.bg_dark{
  position: relative;
  background-color: #1e1c1c;
  min-height: 600px;
  overflow: hidden;

  .bg_title {
    position: absolute;
    top: -65px;
    left: 50%;
    transform: translateX(-50%);
    font-family: $title_font;
    font-size: 230px;
    color: #181515;
    font-weight: 600;
  }

  .content{
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    display: flex;
    justify-content: space-between;
    align-items: center;

    .left, .right {
      color: white;
    }
  }
}

</style> 
