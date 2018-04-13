<template>
  <div class="header">
    <div class="nav">
      <router-link :to="{path:'/'}" :class="[path === '/' ? 'active' : '']">首页</router-link>
      <router-link :to="{path:'/about'}" :class="[path === '/about' ? 'active' : '']">关于</router-link>
    </div>
  </div>
</template>

<script>
export default {
  computed: {
    path() {
      return this.$route.path
    }
  }
}
</script>

<style lang="scss">
body {
  background: #e2e2e2;
}

.header {
  height: 40px;
  line-height: 40px;
  background: #fff;
  // background: hsla(0,0%,100%,0);
  margin-bottom: 20px;
  text-align: center;
  .nav {
    a {
      color: #778087;
      font-size: 18px;
      font-weight: 500;
      text-decoration: none;
      padding: 0 8px;
      &:first-child {margin-right: 10px;}
      &.active {
        border-bottom: 2px solid #778087;
      }
    }
  }
}
</style>

