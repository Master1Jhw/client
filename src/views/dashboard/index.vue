<template>
  <div class="dashboard-container">
    <div class="dashboard-text">你好， {{ name }}，欢迎进入实验室信息管理系统</div>
      <div align="left"><font color="red">功能说明：</font></div>
      <div align="left"><font color="black">教师在添加课程后，可通过课程进行实验室预约</font></div>
      <div align="left"><font color="black">教师预约后需要经过管理员审核，才可在已审核信息中查到相关预约</font></div>
      <div align="left"><font color="black">一经预约则同时间实验室资源即被锁定，无法被再次预约，除非审核被否定，则释放资源</font></div>
  </div>
</template>

<script>
import { mapGetters } from 'vuex'

export default {
  name: 'Dashboard',
  computed: {
    ...mapGetters([
      'name'
    ])
  }
}
</script>

<style lang="scss" scoped>
.dashboard {
  &-container {
    margin: 30px;
  }
  &-text {
    font-size: 30px;
    line-height: 46px;
  }
}
</style>
