<template>
  <div class="app-wrapper">
    <sidebar class="sidebar-container"></sidebar>
    <div class="main-container">
      <navbar/>
      <app-main/>
    </div>
  </div>
</template>

<script>
import AppMain  from '@/views/layout/components/AppMain'//页面布局的右侧区域
import sidebar  from '@/views/layout/components/sidebar'//页面布局的左侧菜单
import Navbar  from './Navbar'
// import './index.scss'

export default {
  name: 'layout',
  components: {
    AppMain,
    sidebar,
    Navbar
  }
}
</script>

<style scoped>
.app-wrapper {
  position: relative;
  height: 100%;
  width: 100%;
}
.main-container{
  min-height: 100%;
    transition: margin-left 0.28s;
    margin-left: 180px;
}
.sidebar-container {
    transition: width 0.28s;
    width: 180px!important;
    height: 100%;
    position: fixed;
    top: 0;
    bottom: 0;
    left: 0;
    z-index: 1001;
    /* text-align: center */
  }
  .sidebar-container a{
    display: inline-block;
    width: 100%;
  }
  .sidebar-container .svg-icon{
   margin-right: 16px;
  }
  .sidebar-container .el-menu{
    border: none;
      width: 100%;
  }
</style>
<style>
.el-submenu .el-menu-item{
    min-width: 180px!important;
  }
</style>

