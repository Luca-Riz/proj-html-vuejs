<template>
  <div class="cont sec5 mt-4">

    <!-- title -->
    <div class="title text-center">
      <div class="title titleFont fw-bolder">Latest news<span class="master_orange">.</span></div>
      <div class="sub_title t_grey">Lorem ipsum dolor sit amet, consectetur adipisicing elit.</div>
      <div class="line"></div>
      
    </div>
    <!-- end title -->

    <!-- main -->
    <div class="container main d-flex justify-content-between">
      <div class="row mt-4">
        <div v-for="(item,i) in Sec5" :key="i" class="circle col-4">
          <div class="image">
            <img :src="item.url" :alt="item.title">
          </div>

          <div class="tag bg_orange">
            <span class="me-1">
              <i class="bi bi-tag"></i>
            </span>
            <span>Business, Leading</span>
          </div>

          <!-- text below img -->
          <div class="aboveTitle d-flex mt-5">
            <div class="date">
              <span class="master_orange me-1">
                <i class="bi bi-clock"></i>
                </span> 
              <span class="t_grey me-1">May 5, 2019</span>               
            </div>
            <div class="who">
              <span class="master_orange me-1">
                <i class="bi bi-person"></i>
                </span> 
              <span class="t_grey">Amanda Doe</span>  
            </div>
          </div>
          <div class="fw-bolder fs-3 mt-1 mb-2 titleFont subTitle"> {{item.title}} </div>
          <div class="t_grey mb-3"> {{item.text}} </div>
          <div class="text-uppercase fw-bolder cP link">
            <span>Read more</span> 
          </div>
          <!-- end text below img -->
        </div>
      </div>
    </div>
    <!-- end main -->

    <div class="points">
      <img src="../assets/svg/svg-4.svg" alt="pointing2">
    </div>


  </div>
</template>

<script>
import Sec5 from '@/data/Sec5.js';

export default {
  name: 'Section1',
  data() {
    return {
      Sec5
    }
  },
}
</script>

<style lang="scss" scoped>
@import '../style/common.scss';

.sec5{
  position: relative;
  transform: translate(0, -60px);
  padding-top: 130px;
  padding-bottom: 80px;

  .title{

    .title{
      font-size: $fSize_2;
      font-family: $title_font;
    }
  }


    .sub_title{
      margin-bottom: 2rem;
    }
    
    .line{
      width: 80px;
      height: 2px;
      background-color: $m_orange;
      margin: auto;
      margin-bottom: $fSize_2;
    }
  
  .main{
    width: 70%;
    margin:auto;

    .circle{
      position: relative;

      .link{
      position: relative;
      display: inline-block;
      }

      .link:hover::after{
      position: absolute;
      content: url('../assets/svg/arrow-right.svg');
      top: 2px;
      right: -25px;
      }
      
      .aboveTitle{
        font-size: $fSize_7;
      }

      .image{
        cursor: pointer;
        overflow: hidden;

        img{
          transition: 0.5s;
          width: 100%;

          &:hover {
            transform: scale(1.05);
            }
          };

      }

      .tag {
        position: absolute;
        top: 225px;
        right: 30px;
        padding: 10px 20px;
      }

      .subTitle{
        font-size: $fSize_4;
      }

    }

  }

  .points{
    position: absolute;
    left:0;
    top:-40px;
    z-index: -1;
  }

}
</style> 
