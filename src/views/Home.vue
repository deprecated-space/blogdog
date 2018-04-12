<template>
  <div class="main">
    <div class="item" v-for="item in articleList" :key="item.id" >
      <span class="title">
        <router-link 
          :to="{
            path: `/post/${item.year}/${item.title}`
          }"
          >
          {{ item['title-zh'] }}
        </router-link>
      </span>
      <span class="date">{{ item.date }}</span>
    </div>
  </div>
</template>

<script>
import {articleList} from '@/config'

export default {
  data() {
    return {
      articleList: articleList
    }
  }
}
</script>

<style lang="scss">
.main {
  // min-width: 200px;
  // max-width: 980px;
  width: 580px;
  margin: 0 auto;
  padding: 45px;
  background: #fff;
  .item {
    padding-bottom: 5px;
    .title > a {
      color: #778087;
      text-decoration: none;
    }
    .date {float: right; color: #778087;}
  }
}
</style>

