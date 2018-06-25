<template>
  <div class="yun-page">
    <div class="lnav" :class="{ lnavhid: isCollapse }">
      <!-- :class="lnavhid?!isCollapse:false" -->
      <div class="lnav-top" :class="{ lnavhid: isCollapse }">
        <img src="~static/index/logo.png" alt="">
        <h1 class="title" v-show="!isCollapse">云图在线</h1>
      </div>
      <div class="lnav-content">
        <!-- <el-tree :data="data" highlight-current="true" accordion="true" :props="defaultProps" @node-click="handleNodeClick"></el-tree> -->
        <!-- <el-radio-group v-model="isCollapse" style="margin-bottom: 20px;">
          <el-radio-button :label="false">展开</el-radio-button>
          <el-radio-button :label="true">收起</el-radio-button>
        </el-radio-group> -->
        <el-menu default-active="1-4-1" class="el-menu-vertical-demo nav-menu" :class="{ lnavhid: isCollapse }" @open="handleOpen" @close="handleClose" :collapse="isCollapse" 
        background-color="black" text-color="#fff" active-text-color="red">
          <!-- <el-menu-item index="0">
            <i class="lnav-top"><img src="~static/index/logo.png" alt=""></i>
            <span slot="title" class="title">云图在线</span>
          </el-menu-item> -->
          <!-- <el-menu-item index="2">
            <i class="el-icon-menu"></i>
            <span slot="title">导航二</span>
          </el-menu-item> -->
          <el-submenu index="1">
            <template slot="title">
              <i class="el-icon-location"></i>
              <span slot="title">导航一</span>
            </template>
            <el-menu-item-group>
              <span slot="title">分组一</span>
              <el-menu-item index="1-1">选项1</el-menu-item>
              <el-menu-item index="1-2">选项2</el-menu-item>
            </el-menu-item-group>
            <el-menu-item-group title="分组2">
              <el-menu-item index="1-3">选项3</el-menu-item>
            </el-menu-item-group>
            <el-submenu index="1-4">
              <span slot="title">选项4</span>
              <el-menu-item index="1-4-1">选项1</el-menu-item>
            </el-submenu>
          </el-submenu>
          <el-menu-item index="2">
            <i class="el-icon-menu"></i>
            <span slot="title">导航二</span>
          </el-menu-item>
          <el-menu-item index="3" disabled>
            <i class="el-icon-document"></i>
            <span slot="title">导航三</span>
          </el-menu-item>
          <el-menu-item index="4">
            <i class="el-icon-setting"></i>
            <span slot="title">导航四</span>
          </el-menu-item>
        </el-menu>
      </div>
      
      <!-- <el-radio-group v-model="isCollapse" style="margin-bottom: 20px;">
        <el-radio-button :label="!isCollapse">展开</el-radio-button>
      </el-radio-group> -->
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
  }
</style>
