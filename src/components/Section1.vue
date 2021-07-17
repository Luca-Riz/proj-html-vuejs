<template>
  <div class="cont sec1">

    <!-- title -->
    <div class="title text-center">
      <div class="titleFont fw-bolder">Our specialities<span class="orange">.</span></div>
      <div class="sub_title">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Veniam, consequuntur?</div>
      <div class="line"></div>
      
    </div>
    <!-- end title -->

    <!-- main -->
    <div class="main d-flex justify-content-between">
      <div v-for="(item,i) in SecOurSpec" :key="i" class="circle">
        <div class="m-4">
          <img :src="item.url" :alt="item.title">
        </div>
        <div class="fw-bolder mb-2"> {{item.title}} </div>
        <div> {{item.text}} </div>
      </div>
    </div>
    <!-- end main -->


  </div>
</template>

<script>
import SecOurSpec from '@/data/SecOurSpec.js';

export default {
  name: 'Section1',
  data() {
    return {
      SecOurSpec
    }
  },
}
</script>

<style lang="scss" scoped>
@import '../style/common.scss';

.sec1{
  position: relative;
  transform: translate(0, -60px);
  background-color: white;
  padding-top: 130px;
  padding-bottom: 130px;

    .titleFont{
      font-size: $fSize_2;
      font-family: $title_font;
    }

    .sub_title{
      margin-bottom: 2rem;
    }
    
    .line{
      width: 80px;
      height: 2px;
      background-color: $orange;
      margin: auto;
      margin-bottom: $fSize_2;
    }
  
  .main{
    text-align: center;
    width: 70%;
    margin:auto;

    .circle{
      width: 20%;

    }
  }

}
</style> 
