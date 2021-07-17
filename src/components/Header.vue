<template>
  <div class="allHead">

    <div class="container-fluid">

      <!-- start header -->
      <header class="d-flex justify-content-between">
        <!-- left -->
        <div class="titleFont fs-1 m-3"> Everlead<span class="orange">.</span></div>
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

      <div class="jumbotron">
        <div class="ourTeam row d-flex">

          <div class="sx col-1">
            <!--arrow left-->
            <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" fill="currentColor" class="bi bi-arrow-left" viewBox="0 0 16 16">
              <path fill-rule="evenodd" d="M15 8a.5.5 0 0 0-.5-.5H2.707l3.147-3.146a.5.5 0 1 0-.708-.708l-4 4a.5.5 0 0 0 0 .708l4 4a.5.5 0 0 0 .708-.708L2.707 8.5H14.5A.5.5 0 0 0 15 8z"/>
            </svg>
            <!--end arrow left-->
          </div>

          <div class="center col-4">
            <div class="titleFont fw-bolder">Our Team<span class="orange">.</span></div>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Sit delectus molestiae eius iure debitis!</p>
            <div class="">
              <!--# da sistemare -->
              <div class="text-uppercase inline_b">Read more</div>
              <div class="text-uppercase inline_b bg_orange">Purchase</div>
            </div>
          </div>

          <div class="dx col-1 offset-6">
            <!-- arrow right -->
            <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20"  fill="currentColor" class="bi bi-arrow-right" viewBox="0 0 16 16">
              <path fill-rule="evenodd" d="M1 8a.5.5 0 0 1 .5-.5h11.793l-3.147-3.146a.5.5 0 0 1 .708-.708l4 4a.5.5 0 0 1 0 .708l-4 4a.5.5 0 0 1-.708-.708L13.293 8.5H1.5A.5.5 0 0 1 1 8z"/>
            </svg>
            <!--end arrow right-->
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
