<template>
  <div id="app">
    <Top/>
    <router-view class="site-content"/>
    <Bottom/>
  </div>
</template>

<script>
import Top from '@/components/Top'
import Bottom from '@/components/Bottom'

export default {
  components: {
    Top, Bottom
  }
}
</script>

<style>
* {margin: 0; padding: 0}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  /* margin-top: 60px; */

  display: flex;
  min-height: 100vh;
  flex-direction: column;
}

.site-content {
  flex: 1;
  background: #fff;
}
</style>
