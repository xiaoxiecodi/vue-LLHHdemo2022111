<template>
  <el-button type="text" @click="open">点击打开AlertMessageBox</el-button>
</template>

<script>
export default {
  methods: {
    open() {
      this.$alert('这是一段内容', '标题名称alert提示', {
        confirmButtonText: '确定',
        callback: (action) => {
          this.$message({
            type: 'info',
            message: `action: ${action}`,
          });
        },
      });
    },
  },
};
</script>
