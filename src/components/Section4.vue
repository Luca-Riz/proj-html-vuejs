<template>
  <div class="all">
    <div class="container">
      <div class="row">
        
        <div class="col-6 left px-5">
          <div class="titleFont fw-bolder pb-2">
            Creative Leader<span class="master_orange">.</span>
          </div>
          <div class="line"></div>
          <p class="pt-3">
          Lorem ipsum dolor sit, amet consectetur adipisicing elit.Quis pariatur adipisci ea cum nobis quaerat. Placeat in,excepturi eligendi, cupiditate deserunt consecteturveniam sed atque doloribus assumenda, libero corporis?Aperiam.
          Molestiae ut alias reprehenderit eos repellat sapiente porro nihil laboriosam.
          </p>
          <div class="text-uppercase fw-bolder cP link">
            <span>Read more</span> 
          </div>
        </div>

        <div class="col-6 right">
          <div class="mentor" v-for="item in SecCreative" :key="item.id">
            <div class="name d-flex justify-content-between titleFont my-1">
              <div class="sx"> {{item.title}} </div>
              <div class="dx"> {{item.perc}} </div>
            </div>
            <div class="bar">
              <div class="all"></div>
              <div class="perc" :class="`${item.w}`"></div>

            </div>
          </div>
        </div>
      </div>
    



    </div>
  </div>
</template>


<script>

import SecCreative from "@/data/SecCreative.js"
export default {
  name: 'Section4',
  data() {
    return {
      SecCreative
    }
  },
}
</script>

<style lang="scss" scoped>
@import '../style/common.scss';

.all{
  background-color: white;
  border: 1px solid white; //per fragare boostrap
}

.container{

  .row{
    margin-top: 100px;
    margin-bottom: 100px;

    .left{
      width: 50%;
  
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



      .titleFont{
        font-size: $fSize_3;
      }
  
      p{
        color: $t_grey;
      }
    
      .line{
        width: 75px;
        height: 2px;
        background-color: $m_orange;
      }
    }
    
    .right{
      width: 50%;
  
      .mentor{
        margin-bottom: 35px
      }
  
      .name{
        font-size: $fSize_4;
        font-weight: 600;
      }
    
      .bar{
        position: relative;
        
          .all{
            position: absolute;
            top: 3px;
            left: 0;
            width: 100%;
            height: 3px;
            background-color: $border_grey3;
          }
    
        .perc{
          position: absolute;
          top: 0;
          left: 0;
          height: 5px;
          background-color: $m_orange;
        }
  
        .w78{width: 78%;}
        .w95{width: 95%;}
        .w65{width: 65%;}
        .w83{width: 83%;}
      }
    }
  }


}

</style> 
