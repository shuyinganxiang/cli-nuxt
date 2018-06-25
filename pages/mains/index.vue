<template>
  <div>  
    <left-nav class="left-nav" :isCollapse="isCollapse" />
    <top-nav class="top-nav" :class="{ lnavhid: isCollapse }" @collapse="collapse"></top-nav>
    <contents class="contents" :class="{ lnavhid: isCollapse }"></contents>
      <!-- <el-radio-group v-model="isCollapse" style="margin-bottom: 20px;">
        <el-radio-button :label="!isCollapse">展开</el-radio-button>
      </el-radio-group> -->

    <!-- <p>项目demo-默认布局中的内容</p> -->
    <!-- <nuxt/> -->
  </div>
</template>

<script>
  import leftNav from '../../components/common/leftNav'
  import topNav from '../../components/common/topNav'
  import contents from '../../components/mains/content.vue'
  export default {
    components:{
      leftNav,
      topNav,
      contents
    },
    data() {
      return {
        isCollapse: true
      };
    },
    methods: {
      collapse(param) {
        this.isCollapse = param
        // alert(isCollapse)
      }
    }
  }
</script>


<style scoped>
  .left-nav {
    float: left;
  }
  .top-nav {
    /* float: left; */
    margin-left: 256px;
    background-color: deeppink;
  }
  .contents {
    margin-left: 256px;
    height: 300px;
    background-color: greenyellow;
  }
  .lnavhid {
    margin-left: 80px;
  }
</style>
