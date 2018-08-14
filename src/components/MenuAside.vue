<template>
  <el-menu :default-active="$route.path"
           background-color="#545c64"
           text-color="#fff"
           active-text-color="#ffd04b" :collapse="isCollapse" :router="true" tag="div">
    <li><menu-list :data="menuData"></menu-list></li>
  </el-menu>
</template>

<script>import MenuList from './MenuList.vue';
export default {
  name: 'MenuAside',
  data () {
    return {
      activeIndex: '1',
      isCollapse: false,
      menuData: [
        {
          iconClass: ['el-icon-menu'], toHref: '/home', text: '主页', children: []
        },
        {
          iconClass: ['el-icon-menu'], toHref: '', text: '基本组件', children: [
            {iconClass: [], toHref: '/color', text: 'color', children: []},
            {iconClass: [], toHref: '/font', text: 'icon字体', children: []}
          ]
        },
        {
          iconClass: ['el-icon-menu'], toHref: '/layout', text: 'layout布局', children: []
        },
        {
          iconClass: ['el-icon-menu'], toHref: '/plugins', text: '常用插件', children: []
        },
        {
          iconClass: ['el-icon-menu'], toHref: '/', text: '主页', children: []
        }
      ]
    };
  },
  methods: {
    tab(){
      this.isCollapse = !this.isCollapse;
    }
  },
  components: {
    MenuList
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
