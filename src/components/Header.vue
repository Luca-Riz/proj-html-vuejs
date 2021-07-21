<template>
  <div class="allHead">

    <div class="container-fluid">

      <!-- start header -->
      <header class="d-flex justify-content-between">
        <!-- left -->
        <div class="titleFont fs-1 m-3">Everlead<span class="master_orange">.</span></div>
        <!-- end left -->
        
        <!-- right -->
        <nav class="upRight">
          <ul class="none d-flex justify-content-start">
            <li v-for="item in NavBarHeader" :key="item"
              class="text-uppercase unstyled m-3 cP">
                <i class="bi bi-arrow-right"></i>
                <strong>{{ item }}</strong>
            </li>
            <li class="m-3 cP"> 
              <i class="fas fa-search"></i> 
            </li>
            <li class="m-3 cP">
              <i class="fas fa-list-ul"></i> 
            </li>
          </ul>
        </nav>
        <!-- end right -->

      </header>
      <!-- end header -->

      <div class="jumbotron">
        <div class="ourTeam row d-flex">

          <div class="sx col-1">
            <i class="bi bi-arrow-left cP"></i>
          </div>

          <div class="center col-4">
            <div class="titleFont fw-bolder">
              Our Team<span class="master_orange">.</span>
            </div>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Sit delectus molestiae eius iure debitis!</p>
            <div class="btn_arrow">
              <div class="text-uppercase inline_b cP">
                <span>Read more</span> 
                <div class="oLine c_bl"></div>
                <i class="bi bi-arrow-right"></i>
              </div>
              <div class="text-uppercase inline_b bg_orange cP">
                <span>Purchase</span> 
                <div class="oLine c_wi"></div>
                <i class="bi bi-arrow-right"></i>
              </div>
            </div>
          </div>

          <div class="dx col-1 offset-6">
            <i class="bi bi-arrow-right cP"></i>
          </div>

        </div>
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
@import '../style/header.scss';

</style>
