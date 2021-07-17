<template>
  <div class="cont sec2 debug">

    <div class="img">
      <img src="../assets/img/h1-blog-img-04.jpg" alt="">
    </div>

    <div class="point">
      <img src="../assets/svg/svg-4.svg" alt="pointing">
    </div>

    <div class="jason debug">
      <div class="titleFont"> Jason Bickford </div>
      <div class="subTitle"> Founder and Executive Director </div>
      <div class="bg_orange"></div>
      <p class=""> Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua... </p>
      <div class="social">
        <div> <i class="fab fa-linkedin-in"></i> </div>
        <div> <i class="fab fa-facebook-f"></i> </div>
        <div> <i class="fab fa-twitter"></i> </div>

      </div>
    </div>


  </div>
</template>

<script>

export default {
  name: 'Section2',

}
</script>

<style lang="scss" scoped>
@import '../style/common.scss';

.sec2{
  height: 700px;
  position: relative;
  padding: auto;


  .img{
    height: 500px;
    margin-top: 100px;
    margin-left: 200px;
    display: inline-block;
    overflow: hidden;

    img{
      height: 100%;
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
    right: 230px;
    transform: translateY(-50%);
    background-color: white;
    width: 650px;
    height: 400px;

    .titleFont{
      font-size: $fSize_2;
    }

    .bg_orange{
      width: 75px;
      height: 2px;
    }

    .social div{
      display: inline-block;
      width: 2rem;
      height: 2rem;
      background-color: $orange;
      border-radius: 50%;
      position: relative;

      i{
        background-color:white;
        position: absolute;
        top: 50%;
        left: 50%;
      }
    }
  }

  .jason .social div i{
    color:white;
    position:absolute;
    top: 50%;
    left: 50%;
    // transform: translate( -50%, -50%);
  }

}





</style> 
