<template>
  <div>
    <h2>News-Content {{$route.params.id}}</h2>
    <ul>
      <li><nuxt-link :to="{name:'index'}">HOME</nuxt-link></li>
    </ul>
  </div>
</template>

<script>
  export default {
    validate ({ params }) {
      // Must be a number 当news/index.vue 中，文件的路由不是数字时，报错误页面
      return /^\d+$/.test(params.id)
    },
    data() {
      return {
        title:this.$route.params.title
      }
    },
    head(){ // 每个页面设置的
      return{
        title:this.title,
        meta:[
          {hid:'description',name:'news',content:'This is news page'}
        ]
      }
    }
  }
</script>