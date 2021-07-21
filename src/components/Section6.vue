<template>
  <div class="bg_dark">
    <div class="bg_title">Testimonials.</div>

    <div class="content">

      <div class="left fs-2">
        <i class="bi bi-arrow-left" @click="prevImg"></i>
      </div>

      <!-- center -->
      <div class="center">
        <div class="image">
          <img :src="Sec6[count6].url" alt="">
        </div>
        <div class="name titleFont fw-bolder my-4"> {{Sec6[count6].name}} </div>
        <div class="text mb-4"> {{Sec6[count6].text}} </div>

        <div class="scrollbar d-flex justify-content-center align-item-center">

          <div class="num_l mx-2"> 0{{count6+1}} </div>
          <div class="bar">
            <div class="navig cP" :class="(index == count6) ? 'attiva' : 'disattiva'" v-for="      (element,index) in Sec6" :key="index" @click="navImg(index)"></div>
          </div>
          <div class="num_r mx-2">03</div>

        </div>
      </div>
      <!-- end center -->

      <div class="right fs-2">
        <i class="bi bi-arrow-right" @click="nextImg"></i>
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
      Sec6,
      count6: 0,
    }
  },

  methods: {
    nextImg(){
      this.count6++;
      if(this.count6 == this.Sec6.length){
        this.count6 = 0
      }
    },

    prevImg(){
      this.count6--;
        if(this.count6 < 0){
          this.count6 = this.Sec6.length-1
        }
      },

    navImg(i) {
      this.count6 = i;
    }, 


  }
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
          display: flex;
          justify-content: flex-start;
          align-items: center;

          .attiva {background-color: white;}
          .disattiva {background-color: #6a6a6a;}

          .navig{
            top: 50%;
            width: calc(100%/3);
            height: 1px;
            // background-color: #6a6a6a;
          }

          
        }
      }
    }

  }
}

</style> 
