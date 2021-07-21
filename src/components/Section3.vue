<template>

  <div class="sec3">

    <!-- rectangle over the photo -->
    <div class="upEvent">

      <div class="top">
        <div class="upcoming titleFont fs-2 fw-bolder mt-4 ms-5">Upcoming Events</div>
      </div>

      <div class="other">

        <div class="event d-flex justify-content-start cP" v-for="(item,i) in SecUpEvent" :key="i">

          <div class="sx bg_orange text-center mt-3 ms-5">
            <div class="day titleFont fw-bolder"> {{item.day}} </div>
            <div class="date mb-2 mx-2"> {{item.date}} </div>
          </div>

          <div class="dx ms-4">
            <div class="city titleFont fw-bolder"> {{item.city}} </div>
            <div class="txt hour my-2 t_grey">
              <i class="bi bi-clock me-2"></i> 
              {{item.hour}} 
            </div>
            <div class="txt address my-2 t_grey">
              <i class="bi bi-geo-alt me-2"></i>
              {{item.address}} 
            </div>
            <div class="cLink">
              <div class="link text-uppercase fw-bolder my-2"> {{item.link}} </div>
            </div>
          </div>
        </div>

      </div>


    </div>
    <!-- end rectangle over photo -->

  </div>
</template>

<script>
import SecUpEvent from '@/data/SecUpEvent.js';

export default {
  name: 'Section3',
  data() {
    return {
      SecUpEvent
    }
  },
}
</script>

<style lang="scss" scoped>
@import '../style/common.scss';

.sec3{
  height: 1050px;
  width: 100%;
  background-image: url("../assets/img/h1-img-09.jpg");
  background-position: top;
  background-repeat: no-repeat;
  position: relative;

  .upEvent{
    width: 500px;
    background-color: white;
    position: absolute;
    top: 50%;
    left: 16%;
    transform: translateY(-50%);
  }

  .upcoming{
      margin-bottom: 30px;
      

  }

  .event{
    padding-top: 28px;
    padding-bottom: 28px;
    border-top: 1px solid #ebebeb;

    .city{
      transition: 0.3s;
    }

    .city:hover {
      color: $m_orange;
    }

    .cLink{
      overflow: hidden;
    }

    .link{
      position: relative;
      display: inline-block;
      transition: 0.3s;
      padding-right: 40px;
    }

    .link:before{
      position: absolute;
      content: url('../assets/svg/arrow-right.svg');
      top: 2px;
      left: -25px;
    }

    .link:hover{
      transform: translateX(30px);
    }



    .sx, .dx{
      display: inline-block;
    }

    .bg_orange{
      background-color: $m_orange;
    }

    .sx{
      height: 50%;


      .day{font-size: $fSize_4;}
      .date{font-size: $fSize_7;
          line-height: 0.8;
          }
    }

    .dx {
      .city{
        font-size: $fSize_4;
      }

      }.txt{
        font-size: $fSize_7;
    }

    .dx i{
      color: $m_orange;
    }
  }
}

</style> 
