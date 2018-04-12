<template>
  <div class="header">
    <div class="nav">
      <router-link :to="{path:'/'}">首页</router-link>
      <router-link :to="{path:'/about'}">关于</router-link>
    </div>
  </div>
</template>

<style lang="scss">
body {
  background: #e2e2e2;
}

.header {
  height: 40px;
  line-height: 40px;
  background: #fff;
  margin-bottom: 20px;
  .nav {
    float: right;
    margin-right: 50px;
    a {
      color: #556;
      font-size: 18px;
      font-weight: 500;
      text-decoration: none;
      margin-right: 5px;
    }
  }
}
</style>

