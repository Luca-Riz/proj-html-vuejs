<template>
  <div>
    <div class="container">
      <div class="row">
        
        <div class="col-6 left debug">
          <div class="titleFont fw-bolder">
            Creative Leader<span class="orange">.</span>
          </div>
          <div class="line"></div>
          <p>
          Lorem ipsum dolor sit, amet consectetur adipisicing elit.Quis pariatur adipisci ea cum nobis quaerat. Placeat in,excepturi eligendi, cupiditate deserunt consecteturveniam sed atque doloribus assumenda, libero corporis?Aperiam.
          Molestiae ut alias reprehenderit eos repellat sapiente porro nihil laboriosam, delectus sequi rerum aliquid autem maxime minus iusto commodi ullam neque, culpa dolor. Iure iusto esse inventore, dolor minima possimus.
          </p>
          <div class="text-uppercase fw-bolder cP">Read more</div>
        </div>

        <div class="col-6 right debug">
          <div class="mentor" v-for="item in SecCreative" :key="item.id">
            <div class="name d-flex justify-content-between">
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

.container{


  .left{
    width: 50%;

    .titleFont{
      font-size: $fSize_3;
    }

    p{
      color: $t_grey;
    }
  
    .line{
      width: 75px;
      height: 2px;
      background-color: $orange;
    }
  }
  
  .right{
    width: 50%;
  
    .bar{
      position: relative;
      
        .all{
          position: absolute;
          top: 4px;
          left: 0;
          width: 100%;
          height: 1px;
          background-color: $bg_grey;
        }
  
      .perc{
        position: absolute;
        top: 0;
        left: 0;
        height: 5px;
        background-color: $orange;
      }

      .w78{width: 78%;}
      .w95{width: 95%;}
      .w65{width: 65%;}
      .w83{width: 83%;}
    }
  }
}

</style> 
