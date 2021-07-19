<template>
  <div class="container">

    <div class="top row d-flex align-items-center">

      <!-- left -->
      <div class="left col-6 pe-4">
        <img src="../assets/img/h1-contact-rev-01.png" alt="world" class="world">
        <div class="p1">
          <img src="../assets/img/h1-contact-rev-02.png" alt="plus1">
          <div class="position shadow px-5 py-3 mt-3">
            <div class="where titleFont fw-bolder">New York coacing</div>
            <div class="more text-uppercase cP fw-bolder">Read More</div>
          </div>
        </div>
        <img src="../assets/img/h1-contact-rev-02.png" alt="plus2" class="p2">
        <img src="../assets/img/h1-contact-rev-02.png" alt="plus3" class="p3">
      </div>
      <!-- end left -->

      <!-- right -->
      <div class="right col-6 ps-4">
        <div class="titleFont h fw-bolder">Contact us
          <span class="master_orange">.</span> 
        </div>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
        <div class="line"></div>
        <div class="nameMail d-flex">
          <div class="name">
            <input type="text" placeholder="Your name">
          </div>
          <div class="mail">
            <input type="email" placeholder="Your Email">
          </div>
        </div>
        <div class="message">
          <textarea rows="3" cols="" name="comment" form="usrform">
            Write a message...
          </textarea>
        </div>
        <div class="send bg_orange text-uppercase">
          <span>Send</span>
          <i class="bi bi-arrow-bar-right"></i>
        </div>
      </div>
      <!-- end right -->

    </div>

    <!-- bottom logo brands -->
    <div class="brands bottom container d-flex justify-content-between">
      <div class="img1">
        <img src="../assets/img/h4-clients-img-03.png" alt="">
      </div>
      <div class="img2">
        <img src="../assets/img/h4-clients-img-05.png" alt="">
      </div>
      <div class="img3">
        <img src="../assets/img/h4-clients-img-07.png" alt="">
      </div>
      <div class="img4">
        <img src="../assets/img/h4-clients-img-09.png" alt="">
      </div>
      <div class="img5">
        <img src="../assets/img/h4-clients-img-01.png" alt="">
      </div>
    </div>
    <!-- bottom logo brands -->

  </div>
</template>

<script>
export default {
  name: 'FooterTop'
}
</script>

<style lang="scss" scoped>
@import '../style/common.scss';
@import '../style/footerTop.scss';

</style>