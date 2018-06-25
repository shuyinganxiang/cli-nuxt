<template>
  <div>
    <!-- <ul>
      <li><nuxt-link :to="{name:'index'}">HOME</nuxt-link></li>
      <li><nuxt-link :to="{name:'about'}">ABOUT</nuxt-link></li>
      <li><nuxt-link :to="{name:'news',params:{newsId:3306}}">NEWS</nuxt-link></li>
      <li><nuxt-link :to="{name:'asyncdata'}">ansycdata</nuxt-link></li>
    </ul>
    <div class="pic"> -->
      <!-- <img src="~static/index/logo.png" alt=""> -->
    <!-- </div>
    <el-radio v-model="radio" label="1">备选项</el-radio>
    <el-radio v-model="radio" label="2">备选项</el-radio>
    <div class="aa">
      <div class="bb">
        <div class="cc">
          测试less
        </div>
      </div>
    </div> -->
  </div>
</template>
 
<script>
 
export default {
  components: {
  },
  data () {
    return {
      radio: '1'
    }
  }
}
</script>
 
 <style>
 
 /* <style lang="less" scoped> */
 .pic{
   width: 100px;
   height: 100px;
   background: url('~static/index/logo.png') no-repeat center center;
   background-size: 100% 100%;
 }
 /* .aa {
   .bb {
     .cc {
       color: blue;
     }
   }
 } */
</style>