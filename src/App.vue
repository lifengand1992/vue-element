<template>
  <el-container class="container">
    <el-aside class="aside" width="200px">
      <menu-aside></menu-aside>
    </el-aside>
    <el-container class="main">
      <el-header class="m-header"></el-header>
      <el-main class="m-main">
        <transition>
          <router-view/>
        </transition>
      </el-main>
    </el-container>
  </el-container>
</template>

<script>import MenuAside from '@/components/MenuAside';
export default {
  name: 'App',
  components: {
    MenuAside
  }
};
</script>

<style lang="scss">
  @import "assets/css/layout.scss";
</style>
