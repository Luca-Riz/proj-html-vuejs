<template>
  <div class="container">

    <!-- start header -->
    <header class="d-flex justify-content-between">
      <!-- left -->
      <div class="titleFont fs-3 m-3"> Everlead <span class="orange">.</span></div>
      <!-- end left -->
      
      <!-- right -->
      <nav class="">
        <ul class="none d-flex justify-content-start">
          <li v-for="item in NavBarHeader" :key="item"
            class="text-uppercase unstyled m-3">
              <strong>{{ item }}</strong>
          </li>
          <li class="m-3"> <i class="fas fa-search"></i> </li>
          <li class="m-3"> <i class="fas fa-list-ul"></i> </li>
        </ul>
      </nav>
      <!-- end right -->

    </header>
    <!-- end header -->

    <div class="jumbotron ">
      <div class="ourTeam row d-flex debug">
        <div class="sx debug col-1">freccia sx</div>
        <div class="center debug col-4">
          <div class="titleFont fw-bolder">Our Team<span class="orange">.</span></div>
          <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Sit delectus molestiae eius iure debitis!</p>
          <div class="">
            <div class="text-uppercase inline_b">Read more</div>
            <div class="text-uppercase inline_b bg_orange">Purchase</div>
          </div>
        </div>
        <div class="dx col-1 offset-6 debug">freccia dx</div>

      </div>
    </div>
    

  </div>
</template>

<script>

import NavBarHeader from '@/data/NavBarHeader.js';

export default {
  name: 'Header', 
  props: {
    msg: String
  },
  data() {
    return {
      NavBarHeader,
    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../style/common.scss';

  .titleFont{
    font-family: "$title_font";
  }

  span.orange { color: $orange}

  .jumbotron {
    background-image: url require('./assets/img/rev-slider-main-home-img-03.jpg');
    .center{
      .titleFont {
        font-size: $fSize_H;
      }

      .inline_b{
        display: inline-block;
      }

    }
  }

</style>
