<template>

  <div class="sec3">

    <!-- rectangle over the photo -->
    <div class="upEvent py-3 px-5">
      <div class="upcoming titleFont fs-2 fw-bolder">Upcoming Events</div>

      <div class="event d-flex justify-content-start" v-for="(item,i) in SecUpEvent" :key="i">

        <div class="sx bg_orange text-center p-2 mt-3">
          <div class="day titleFont fw-bolder"> {{item.day}} </div>
          <div class="date mb-2"> {{item.date}} </div>
        </div>

        <div class="dx ms-4">
          <div class="city titleFont fw-bolder"> {{item.city}} </div>
          <div class="txt hour my-2">
            <i class="bi bi-clock me-2"></i> 
            {{item.hour}} 
          </div>
          <div class="txt address my-2">
            <i class="bi bi-geo-alt me-2"></i>
            {{item.address}} 
            </div>
          <div class="link text-uppercase fw-bolder my-2"> {{item.link}} </div>
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
    height: 670px;
    background-color: white;
    position: absolute;
    top: 50%;
    left: 410px;
    transform: translateY(-50%);
  }

  .upcoming{
      margin-bottom: 70px;

  }

  .event{
    margin-bottom: 60px;

    .sx, .dx{
      display: inline-block;
    }

    .sx{
      height: 50%;

      .day{font-size: $fSize_4;}
      .date{font-size: $fSize_6;
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
      color: $orange;
    }

    
  }
}

</style> 
