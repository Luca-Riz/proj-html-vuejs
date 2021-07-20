<template>
  <div class="all">

    <div class="container">
      <div class="row">

        <!-- about -->
        <div class="about col-3">
          <div class="titleFont">About</div>
          <div class="line"></div>
          <p>
            We created Everlead to effectively become the stepping stone towards meeting all your goals & achieving business success.
          </p>

          <!-- social -->
          <div class="social d-flex">
            <div class="singSoc"> 
              <i class="fab fa-linkedin-in icon"></i> 
            </div>
            <div class="singSoc"> 
              <i class="fab fa-facebook-f icon"></i> 
            </div>
            <div class="singSoc"> 
              <i class="fab fa-twitter icon"></i> 
            </div>
          </div>
          <!-- end social -->
        </div>
        <!-- end about -->

        <!-- twitter -->
        <div class="twitter col-3">
          <div class="titleFont">Twitter</div>
          <div class="line"></div>

          <!-- line 1 -->
          <div class="tw d-flex">
            <div class="logo">
              <i class="fab fa-twitter icon"></i>
            </div>
            <p>
              When it comes to improving your #search #functionality on your #WordPress #site, your first instinct might be to… 
              <a href="#">https://t.co/wLPLptxSKE</a> 
            </p>
          </div>
          <!-- end line 1 -->
          
          <!-- line 2 -->
          <div class="tw d-flex">
            <div class="logo">
              <i class="fab fa-twitter icon"></i>
            </div>
            <p>
              Once the number of #articles on your #blog increases, your older posts will receive less and less traffic as they w…
              <a href="#">https://tN8QX98EiJK</a> 
            </p>
          </div>
          <!--end line 2 -->
        </div>
        <!-- end twitter -->

        <!-- links -->
        <div class="links col-3">
          <div class="titleFont">Important Links</div>
          <div class="line"></div>
          <ul class="">
            <li>About me</li>
            <li>About us</li>
            <li>Language packs</li>
            <li>Become a coach</li>
            <li>Monthly events</li>
          </ul>
        </div>
        <!-- end links -->

        <!-- contact -->
        <div class="contact col-3">
          <div class="titleFont">Contact me</div>
          <div class="line"></div>
          <ul class="">
            <li>
              <i class="bi bi-geo-alt"></i>
              457 BigBlue Street, NY 10013
            </li>
            <li>
              <i class="bi bi-telephone"></i>
              (315) 5512-2579
            </li>
            <li>
              <i class="bi bi-envelope"></i>
              everlead@qodeinteractive.com
            </li>
          </ul>

          <div class="yourName">
            <input type="text" placeholder="Your Name">
            <input class="text-uppercase" type="button" value="Subscribe">
          </div>
          <div class="w_line"></div>
        </div>

        <!-- end contact -->

      </div>
    </div>
  </div>
</template>

<script>

import FooterElement from '@/data/FooterElement.js';
export default {
  name: 'FooterBottom',
  data() {
    return {
      FooterElement
    }
  },
}
</script>

<style lang="scss" scoped>
@import '../style/common.scss';
@import '../style/footerBottom.scss'

</style>