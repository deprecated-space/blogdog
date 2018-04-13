<template>
  <div class="about">
    <h4>如果你对我有兴趣，可以通过以下渠道找到我：</h4>
    <div class="contact">
      <a href="https://github.com/hanzichi" title="GitHub"><img src="https://github.com/favicon.ico"/></a>
      <a href="http://www.cnblogs.com/zichi/" title="cnblogs"><img src="http://www.cnblogs.com/favicon.ico"/></a>
      <a href="https://segmentfault.com/u/hanzichi" title="segmentfault"><img src="https://segmentfault.com/favicon.ico"/></a>
      <a href="https://www.v2ex.com/member/hanzichi" title="v2ex"><img src="https://www.v2ex.com/static/img/icon_rayps_64.png"/></a>
      <a href="https://leetcode.com/hanzichi/" title="leetcode"><img src="https://leetcode.com/favicon.ico"/></a>
      <a href="http://weibo.com/5819145534/profile" title="weibo"><img src="http://weibo.com/favicon.ico"/></a>
    </div>
  </div>
</template>

<script>

export default {
}
</script>

<style lang="scss">
.about {
  // min-width: 200px;
  // max-width: 980px;
  // max-width: 580px;
  margin: 0 auto;
  padding: 45px;
  background: #fff;
  text-align: center;
  .contact {
    margin-top: 15px;
    img {
      width: 32px; height: 32px;
      &:hover {
        opacity: 0.5;
      }
    }
  }
}
</style>

