<template>
  <div>
    <Section1/>
  </div>
</template>

<script>
import Section1 from './Section1.vue'

export default {
  name: 'Main',
  components:{
    Section1
  },
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
