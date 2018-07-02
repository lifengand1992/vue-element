<template>
  <el-menu default-active="1"
           background-color="#545c64"
           text-color="#fff"
           active-text-color="#ffd04b">
    <el-menu-item index="1">
      <template slot="title">
        <router-link to="/home" class="m-link">
          <i class="el-icon-menu"></i>
          <span>主页</span>
        </router-link>
      </template>
    </el-menu-item>
    <el-submenu index="2">
      <template slot="title">
        <i class="el-icon-location"></i>
        <span>基本组件</span>
      </template>
      <el-menu-item index="2-1"><router-link to="/color" class="m-link">color</router-link></el-menu-item>
      <el-menu-item index="2-2">icon字体</el-menu-item>
      <el-menu-item index="2-3">button按钮</el-menu-item>
      <el-menu-item index="2-4">layout布局</el-menu-item>
    </el-submenu>
    <el-menu-item index="4">
      <i class="el-icon-menu"></i>
      <span slot="title">Form</span>
    </el-menu-item>
    <el-menu-item index="3">
      <i class="el-icon-menu"></i>
      <span slot="title">Form</span>
    </el-menu-item>
  </el-menu>
</template>

<script>
export default {
  name: 'MenuAside',
  data () {
    return {
      msg: ''
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  @import "../assets/css/_mixin.scss";
  .is-active .m-link{
    color:#ffd04b;
  }
  .m-link{
    color:#fff;
    display:inline-block;
  }
  .el-menu{
  }
</style>
