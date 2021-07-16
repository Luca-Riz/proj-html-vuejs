<template>
  <div>

    {{ msg }}

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
      headerMenu: NavBarHeader,
    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
