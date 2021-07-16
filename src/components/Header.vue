<template>
  <div>

    <header>
      <!-- left -->
      <div class="compName"></div>
      <!-- end left -->
      
      <!-- right -->
      <nav>
        <ul>
          <li v-for="item in NavBarHeader" :key="item"
            class="text-uppercase">
              {{ item }}
          </li>
        </ul>
      </nav>
      <!-- end right -->

    </header>

    <div class="jumbotron">

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

</style>
