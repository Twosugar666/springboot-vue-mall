<template>
  <el-menu :default-openeds="['1', '3']" style="min-height: 100%; overflow-x: hidden"
           background-color="rgb(48, 65, 86)"
           text-color="#fff"
           active-text-color="#ffd04b"
           :collapse-transition="false"
           :collapse="isCollapse"
           router
  >
    <div style="height: 60px; line-height: 60px; text-align: center">
      <img src="../assets/logo.png" alt="" style="width: 20px; position: relative; top: 5px; right: 5px">
      <b style="color: white" v-show="logoTextShow">东软云商城</b>
    </div>
    <el-submenu index="2">
      <template slot="title">
        <i class="el-icon-shopping-cart-full"></i>
        <span slot="title">商品模块</span>
      </template>
          <el-menu-item index="/user">商品管理</el-menu-item>
          <el-menu-item index="2-4">商品分类管理</el-menu-item>
          <el-menu-item index="2-5">商品类型管理</el-menu-item>
          <el-menu-item index="2-6">品牌管理</el-menu-item>
    </el-submenu>
    <el-submenu index="3">
      <template slot="title">
        <i class="el-icon-tickets"></i>
        <span slot="title">订单模块</span>
      </template>
          <el-menu-item index="3-1">订单管理</el-menu-item>
          <el-menu-item index="3-2">订单设置</el-menu-item>
          <el-menu-item index="3-3">退货申请处理</el-menu-item>
          <el-menu-item index="3-4">退货原因设置</el-menu-item>
    </el-submenu>
    <el-submenu index="4">
      <template slot="title">
        <i class="el-icon-data-analysis"></i>
        <span slot="title">营销模块</span>
      </template>
          <el-menu-item index="4-1">秒杀活动管理</el-menu-item>
          <el-menu-item index="4-2">优惠价管理</el-menu-item>
          <el-menu-item index="4-3">品牌推荐管理</el-menu-item>
          <el-menu-item index="4-4">新品推荐管理</el-menu-item>
          <el-menu-item index="4-5">人气推荐管理</el-menu-item>
          <el-menu-item index="4-6">专题推荐管理</el-menu-item>
          <el-menu-item index="4-7">首页广告管理</el-menu-item>
    </el-submenu>
  </el-menu>
</template>

<script>
export default {
  name: "Aside",
  props: {
    isCollapse: Boolean,
    logoTextShow: Boolean
  },

}
</script>

<style scoped>

</style>