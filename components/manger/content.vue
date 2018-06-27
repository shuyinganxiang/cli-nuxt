<template>
  <div>
    <!-- <h2>manger-content</h2> -->
    <div class="list-add">
      <span class="class-txt">分类</span><list-add class="list-add"/>
      <!-- <el-button class="add-btn" plain><i class="el-icon-circle-plus-outline add-icon"></i>添加</el-button> -->
    </div>
    <el-table :data="tableData2" style="width: 100%" :row-class-name="tableRowClassName">
      <el-table-column prop="date" class="list-top" label="分类"></el-table-column>
      <el-table-column prop="name" class="list-top" label="添加时间"></el-table-column>
      <el-table-column prop="address" class="list-top" label="操作"> </el-table-column>
    </el-table>
    <el-pagination
      background
      :page-size="20"
      :pager-count="11"
      layout="prev, pager, next"
      :total="100">
    </el-pagination>
  </div>
</template>

<script>
  import listAdd from '../../components/manger/listAdd'

  export default {
    components:{
      listAdd
    },
    methods: {
      tableRowClassName({row, rowIndex}) {
        if (rowIndex === 1) {
          return 'warning-row';
        } else if (rowIndex === 3) {
          return 'success-row';
        }
        return '';
      }
    },
    data() {
      return {
        tableData2: [{
          date: '2016-05-02',
          name: '王小虎',
          address: '上海市普陀区金沙江路 1518 弄',
        }, {
          date: '2016-05-04',
          name: '王小虎',
          address: '上海市普陀区金沙江路 1518 弄'
        }, {
          date: '2016-05-01',
          name: '王小虎',
          address: '上海市普陀区金沙江路 1518 弄',
        }, {
          date: '2016-05-03',
          name: '王小虎',
          address: '上海市普陀区金沙江路 1518 弄'
        }]
      }
    }
  }
</script>

<style scoped>
  .list-add{
    height: 32px;
    /* margin-bottom: 6px; */
  }
  .class-txt {
    float: left;
    height: 52px;
    line-height: 32px;
  }
  .add-btn{
    float: left;
    /* height: 32px;
    padding-top: 0;
    line-height: 32px;
    margin-left: 10px; */
  }
  /* .add-icon{
    display: inline-block;
    margin-right: 6px;
  } */
  /* list 的样式 */
  .el-table .warning-row {
    background: oldlace;
    /* background: transparent; */
  }

  .el-table .success-row {
    background: #f0f9eb;
    /* background: transparent; */
  }
  .list-top {
    font-size: 16px;
    font-weight: 400;
    color: #333;
  }
</style>


