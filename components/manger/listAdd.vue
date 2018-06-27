<template>
  <div>
    <el-button class="add-btn" @click="open  " plain><i class="el-icon-circle-plus-outline add-icon"></i>添加</el-button>
    
  </div>
</template>

<script>
  export default {
    methods: {
      open() {
        const h = this.$createElement;
        this.$msgbox({
          title: '添加',
          message: h('p', null, [
            h('span', null, '内容可以是 '),
            h('i', { style: 'color: teal' }, 'VNode')
          ]),
          showCancelButton: true,
          confirmButtonText: '确定',
          cancelButtonText: '取消',
          beforeClose: (action, instance, done) => {
            if (action === 'confirm') {
              instance.confirmButtonLoading = true;
              instance.confirmButtonText = '执行中...';
              setTimeout(() => {
                done();
                setTimeout(() => {
                  instance.confirmButtonLoading = false;
                }, 300);
              }, 3000);
            } else {
              done();
            }
          }
        }).then(action => {
          this.$message({
            type: 'info',
            message: 'action: ' + action
          });
        });
      }
    }
  }
</script>

<style scoped>
  /* .list-add{
    height: 32px;
  }
  .class-txt {
    float: left;
    height: 52px;
    line-height: 32px;
  } */
  .add-btn{
    height: 32px;
    padding-top: 0; /* 清除默认上内边距 */
    line-height: 32px;
    margin-left: 10px;
  }
  .add-icon{
    display: inline-block;
    margin-right: 6px;
  }
  /* list 的样式 */
  /* .el-table .warning-row {
    background: oldlace;
  }

  .el-table .success-row {
    background: #f0f9eb;
  }
  .list-top {
    font-size: 16px;
    font-weight: 400;
    color: #333;
  } */
</style>


