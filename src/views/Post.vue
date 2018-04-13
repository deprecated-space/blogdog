<template>
  <div class="markdown-body post-content" v-html="content">
  </div>
</template>

<script>
import axios from 'axios'
import marked from 'marked'

export default {
  data() {
    return {
      content: ''
    }
  },
  created() {
    let year = this.$route.params.year 
    let title = this.$route.params.title 
    let baseUrl = `https://hanzichi.github.io/blog/posts/${year}/${title}`
    
    axios
      .get(`${baseUrl}/index.md`)
      .then(res => {
        let markdownContent = res.data

        // 图片地址替换
        let p = /(!\[.*\])(\()(.*)\.(.*)(\))/g
      
        console.log(markdownContent)
        
        markdownContent = markdownContent.replace(p, (a, b, c, d, e, f) => {
          return b + c 
            + `${baseUrl}/${d}.${e}` // 完整地址
            + f
        })

        this.content = marked(markdownContent)
      })
  }
}
</script>

<style lang="scss">
.markdown-body {
  // box-sizing: border-box;
  // min-width: 200px;
  // max-width: 980px;
  // width: 100%;
  // margin: 0 auto;
  // padding: 45px;
}

@media (max-width: 767px) {
  .markdown-body {
    padding: 15px;
  }
}
</style>
