<template>
  <div class="bg_dark">
    <div class="bg_title">Testimonials.</div>

    <div class="content">

      <div class="left fs-2">
        <i class="bi bi-arrow-left"></i>
      </div>

      <!-- center -->
      <div class="center" v-for="(item, i) in Sec6" :key="i">
        <div class="image">
          <img :src="item.url" alt="">
        </div>
        <div class="name titleFont fw-bolder my-4"> {{item.name}} </div>
        <div class="text mb-4"> {{item.text}} </div>

        <div class="scrollbar d-flex justify-content-center align-item-center">

          <div class="num_l mx-2">01</div>
          <div class="bar">
            <div class="grey_bar"></div>
            <div class="white_bar"></div>
          </div>
          <div class="num_r mx-2">03</div>

        </div>
      </div>
      <!-- end center -->

      <div class="right fs-2">
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
    color: white;
    width: 90%;

    .left, .right{
      position: relative;

      i{
        position: absolute;
        transition: 0.3s;
        cursor: pointer;
      }
    }

    .left i:hover{
      transform: translateX(-10px);
    }
    .right i:hover{
      transform: translateX(10px);
    }



    .center {
      text-align: center;
      width: 40%;

      .name{
        font-size: $fSize_4;
      }

      .text{
        font-size: $fSize_4;
        color: #a6a6a6;
      }

      .scrollbar{
        color: #c0c0c0;

        .bar{
          width: 150px;
          position: relative;

          .grey_bar{
            position: absolute;
            top: 50%;
            left: 0;
            width: 100%;
            height: 1px;
            background-color: #6a6a6a;
          }

          .white_bar{
            position: absolute;
            top: 50%;
            left: 0;
            width: 30%;
            height: 1px;
            background-color: white;
          }
        }
      }
    }

  }
}

</style> 
