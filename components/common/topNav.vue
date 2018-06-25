<template>
  <div>
    <el-radio-group v-model="isCollapse" style="margin-bottom: 20px;">
      <el-radio-button :label="!isCollapse">展开</el-radio-button>
    </el-radio-group>
    <nuxt />
  </div>
</template>

<script>
export default {
  data() {
    return {
      isCollapse: true
    };
  },
  watch: {
    isCollapse: function(){
      this.$emit('collapse',this.isCollapse)
    }
  }
}
</script>
