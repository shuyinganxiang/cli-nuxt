<template>
  <div class="tnav">
    <div class="dev" @click="collapse"><img src="../../static/index/dev.png" alt=""></div>
    <div class="right">
      <div class="lang">中文</div>
      <!-- <div class="personal">
        <img src="../../static/index/userActor.png" alt="">
        <span>qiaoshemei@163.com</span>
      </div> -->
      <el-dropdown>
        <el-button type="primary" class="personal personal-btn">
          <img src="../../static/index/userActor.png" alt="">
          <span>qiaoshemei@163.com</span>
        </el-button>
        <el-dropdown-menu slot="dropdown" class="btn-list">
          <el-dropdown-item class="btn-exit"><img class="exit-img" src="../../static/index/exit-icon.png" />&nbsp;退出登录</el-dropdown-item>
        </el-dropdown-menu>
      </el-dropdown>
    </div>
    <nuxt />
  </div>
</template>

<script>
export default {
  data() {
    return {
      isCollapse: true,
      formInline: {
        region: ''
      }
    }
  },
  watch: {
    isCollapse: function(){
      this.$emit('collapse',this.isCollapse)
    }
  },
  methods:{
    collapse(){
      this.isCollapse = !this.isCollapse;
      console.log(this.isCollapse)
    },
    handleClick() {
      alert('button click');
    }
  }
}
</script>

<style scoped>
  .tnav {
    height: 64px;
  }
  .dev {
    float: left;
    width: 80px;
    height: 64px;
    line-height: 64px;
    text-align: center;
    cursor: pointer;
  }
  .dev:hover {
    background-color: rgba(167, 202, 214, 0.5);
  }
  .tnav .right{
    float: right;
    margin-right: 12px;
    line-height: 64px;
    /* background-color: yellow; */
  }
  .tnav .right .lang{
    float: left;
    margin-right: 12px;
    color: #1890ff;
    cursor: pointer;
  }
  .tnav .right .personal{
    float: left;
    padding: 0 12px;
    color: rgba(0,0,0,.65);
    cursor: pointer;
  }
  .tnav .right .personal:hover{
    /* background-color: rgba(167, 202, 214, 0.5); */
  }
  .tnav .right .personal img{
    width: 24px;
    height: 24px;
    margin-right: 10px;
    border-radius: 50%;
    vertical-align:middle;
  }
  
  .el-dropdown {
    vertical-align: top;
  }
  .el-dropdown + .el-dropdown {
    margin-left: 15px;
  }
  .el-icon-arrow-down {
    font-size: 12px;
  }
  .personal-btn {
    height: 64px;
    background-color: #fff;
    color: rgba(0,0,0,.65);
    border: none;
  }
  .btn-list {
    margin: 4px 0;
    /* padding-left: 40px; */
  }
  .btn-list .exit-img{
    float: left;
    width: 18px;
    margin-top: 2px;
    vertical-align: middle;
  }
  .btn-exit {
    width: 190px;
    height: 24px;
    line-height: 24px;
    /* vertical-align: middle; */
    /* text-align: center; */
  }
</style>

