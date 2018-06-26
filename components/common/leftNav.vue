<template>
  <div class="yun-page">
    <div class="lnav" :class="{ lnavhid: isCollapse }">
      <div class="lnav-top" :class="{ lnavhid: isCollapse }">
        <img src="~static/index/logo.png" alt="">
        <h1 class="title" v-show="!isCollapse">云图在线</h1>
      </div>
      <div class="lnav-content">
        <el-menu :default-active="$route.path" class="el-menu-vertical-demo nav-menu" :class="{ lnavhid: isCollapse }" @open="handleOpen" @close="handleClose" :collapse="isCollapse" 
        background-color="black" text-color="#fff" active-text-color="red" router>
          <el-menu-item index="/picture">
            <i class="el-icon-picture-outline"></i>
            <span slot="title">图片</span>
          </el-menu-item>
          <el-submenu index="2">
            <template slot="title">
              <i class="el-icon-setting"></i>
              <span slot="title">管理</span>
            </template>
            <div class="child">
              <el-menu-item index="/manger">分类</el-menu-item>
            </div>
          </el-submenu>
        </el-menu>
      </div>
    </div>
  </div>
</template>

<style>
  .el-menu-vertical-demo:not(.el-menu--collapse) {
    width: 200px;
    min-height: 400px;
  }
  /* .is-active {
    background-color: skyblue;
  } */
</style>
<script>
  export default {
    props: {
      isCollapse: {
        type: Boolean,
        default: false
      }
    },
    data() {
      return {
        // isCollapse: true
      };
    },
    methods: {
      handleOpen(key, keyPath) {
        console.log(key, keyPath);
      },
      handleClose(key, keyPath) {
        console.log(key, keyPath);
      }
    },
    created(){
    }
  }
</script>
<style scoped>
  .lnav {
    width: 256px;
    height: 100%;
    /*  */
    background-color: black;
  }
  .lnav-top{
    display: inline-block;
    width: 256px;
    height: 64px;
    line-height: 64px;
    text-align: center;
    color: #fff;
    background-color: rgb(0, 33, 64);
  }
  .lnav img {
    width: 32px;
    margin: 17px 12px 0 24px;
    float: left;
  }
  .lnav .title {
    font-size: 20px;
    float: left;
  }
  .yun-page .lnavhid {
    width: 80px;
    text-align: center;
  }
  .nav-menu{
    width: 256px;
    padding: 16px 0;
    height: 500px;
    border: none;
    border-radius: 50%;
  }
  .child {
    /* border-radius: 50%; */
  }
</style>
