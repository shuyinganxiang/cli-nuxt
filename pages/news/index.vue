<template>
  <div>
    <h2>this is news file</h2>
    <p>NewsID:{{ $route.params.newsId }}</p>
    <ul>
      <li><nuxt-link :to="{name:'index'}">HOME</nuxt-link></li>
      <li>
        <!-- <a href="/news/123">News-1</a> -->
        <nuxt-link :to="{name:'news-id',params:{id:123,title:'i am news'}}">News-1</nuxt-link>
      </li>
      <li><a href="/news/456">News-2</a></li>
    </ul>
  </div>
</template>

<script>
export default {
  // 对应全局设置的css 中的test
  transition:'test'
}
</script>
