<template>
  <div class="">
    <div class="logo-container">
      <el-avatar :size="logoHeight" shape="square" src="http://img.92fa.com/pic/TX1715_01.jpg"></el-avatar>
      <h1 class="logo-title" v-if="$store.getters.sidebarOpened">imooc-admin</h1>
    </div>
    <el-scrollbar>
      <sidebar-menu></sidebar-menu>
    </el-scrollbar>
  </div>
</template>

<script setup>
import SidebarMenu from './SidebarMenu.vue'

const logoHeight = 44
</script>

<style scoped lang="scss">
.logo-container {
  height: v-bind(logoHeight) px;
  padding: 10px 0 22px 0;
  display: flex;
  align-items: center;
  justify-content: center;
  .logo-title {
    margin-left: 10px;
    color: #fff;
    font-weight: 600;
    line-height: 50px;
    font-size: 16px;
    white-space: nowrap;
  }
}
</style>
