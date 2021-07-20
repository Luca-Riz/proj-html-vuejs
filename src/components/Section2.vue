<template>
  <div class="cont sec2">

    <div class="img">
      <img :src="image[count]" :alt="count">
      <div class="aSx cP" @click="prevImg">
        <i class="bi bi-arrow-left"></i>
      </div>
      <div class="aDx cP" @click="nextImg">
        <i class="bi bi-arrow-right"></i>
      </div>
    </div>

    <div class="point">
      <img src="../assets/svg/svg-4.svg" alt="pointing">
    </div>

    <div class="jason">
      <div class="titleFont"> Jason Bickford </div>
      <div class="subTitle t_grey"> Founder and Executive Director </div>
      <div class="bg_orange my-3"></div>
      <p class="t_grey"> 
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua... 
      </p>
      
      <!-- social -->
      <div class="social">
        <div class="singSoc cP"> 
          <i class="fab fa-linkedin-in icon"></i> 
        </div>
        <div class="singSoc cP"> 
          <i class="fab fa-facebook-f icon"></i> 
        </div>
        <div class="singSoc cP"> 
          <i class="fab fa-twitter icon"></i> 
        </div>
      </div>
      <!-- end social -->

      <div class="sign">
        <img src="../assets/img/signJ.jpg" alt="sign">
      </div>
    </div>


  </div>
</template>

<script>

export default {
  name: 'Section2',

  data() {
    return {
      image: [
        require('../assets/img/h1-img-01.jpg'),
        require('../assets/img/h1-img-02.jpg'),
        require('../assets/img/h1-img-03.jpg'),

      ],
      count: 0,
    }
  },

  methods: {
    nextImg(){
      this.count++;
      if(this.count == this.image.length){
        this.count = 0
      }
    },

    prevImg(){
      this.count--;
      if(this.count < 0){
        this.count = this.image.length-1
      }
    }

  },

  mounted(){
    this.interval = setInterval(this.nextImg, 5000);
  }

}
</script>

<style lang="scss" scoped>
@import '../style/common.scss';

.sec2{
  height: 700px;
  position: relative;
  padding: auto;

  .img{
    min-width: 200px;
    position: relative;
    height: 500px;
    margin-top: 100px;
    margin-left: 12%;
    display: inline-block;
    overflow: hidden;

    img{
      height: 100%;
    }

    .aSx, .aDx{
      position: absolute;
      bottom: 0;
      width: 57px;
      height: 71px;
      background-color: $m_orange;
      line-height: 71px;
      text-align: center;
      font-size: 1.5rem;

      i{
        color:white;
      }
    }

    .aSx{
      left: 0;

    }

    .aDx{
      left: 57px;
    }
  }

  .point {
    position:absolute;
    top: 0;
    right: 0;


    img {
      color: $points;
    }
  }

  .jason{
    position: absolute;
    top: 50%;
    left:49%;
    transform: translateY(-50%);
    background-color: white;
    width: 650px;
    height: 400px;
    padding: 70px;

    .titleFont{
      font-size: $fSize_2;
    }

    .bg_orange{
      width: 75px;
      height: 2px;
      background-color: $m_orange;
    }

    .social {
      display: inline-block;

      .singSoc{
        display: inline-block;
        width: 1.8rem;
        height: 1.8rem;
        background-color: $m_orange;
        border-radius: 50%;
        position: relative;
        color: white;
        margin-right: 10px;

        &:hover{
          background-color: black;
        }
      }

      .icon{
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
      }
    }

    .sign{
      height: 4rem;
      display: inline-block;
      text-align: right;
      position: absolute;
      right: 100px;
      top: 240px;

      img{
        height: 100%;
      }
    }
  }


}

</style> 
