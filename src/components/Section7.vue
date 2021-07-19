<template>
  <div>
    <div class="image debug">
      <img src="../assets/img/h1-img-04.jpg" alt="">
      <div class="play">
        <i class="bi bi-play-fill"></i>
      </div>
    </div>

  </div>
</template>

<script>
export default {
  name: 'Section7'
}
</script>

<style lang="scss" scoped>
@import '../style/common.scss';

.image {
  position: relative;
  max-width: 100%;

  img{
    width: 100%;
  }

  .play{
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    color: white;
    font-size: 60px;
  }
}

</style>