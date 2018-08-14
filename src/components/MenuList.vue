<template>
  <div class="menu-list">
    <template v-for="(item, key, index) in data">
      <el-menu-item v-if="item.children.length==0" :index="item.toHref" :key="key">
        <template slot="title">
          <i :class="item.iconClass"></i>
          <span>{{index}}{{item.text}}</span>
        </template>
      </el-menu-item>
      <el-submenu  v-if="item.children.length!=0" :index="item.toHref" :key="key">
        <template slot="title">
          <i :class="item.iconClass"></i>
          <span>{{item.text}}</span>
        </template>
        <menu-list :data="item.children"></menu-list>
      </el-submenu>
    </template>
  </div>
</template>
<script>
export default {
  name: 'MenuList',
  props: {
    data: {
      type: Array
    }
  },
  data () {
    return {
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  @import "../assets/css/_mixin.scss";
  .el-menu{
    border-right:0;
  }
  .el-submenu .el-menu-item,.el-menu-item{
    padding:0;
  }
  .is-active .m-link{
    color:#ffd04b;
  }
  .m-link{
    color:#fff;
    display:block;
  }
</style>
