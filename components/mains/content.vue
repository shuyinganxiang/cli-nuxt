<template>
  <div>
    <h2>content</h2>
    <el-pagination
      background="transparent"
      border="1px solid #ccc"
      :page-size="20"
      :pager-count="11"
      layout="prev, pager, next"
      :total="100">
    </el-pagination>
  </div>
</template>
