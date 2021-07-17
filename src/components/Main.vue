<template>
  <div>
    <Section1/>
    <Section2/>
  </div>
</template>

<script>
import Section1 from './Section1.vue'
import Section2 from './Section2.vue'

export default {
  name: 'Main',
  components:{
    Section1,
    Section2
  },
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
