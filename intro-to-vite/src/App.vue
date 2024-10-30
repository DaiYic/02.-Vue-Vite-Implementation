<template>
  <div id="app">
    <!-- 路由出口，用于渲染匹配的路由组件 -->
    <router-view />
  </div>
</template>

<script setup lang="ts">
// 在这里，你可以导入你需要的组件、库等
// 例如：import { onMounted } from 'vue';

// 你可以在这里使用TypeScript编写你的组件逻辑
</script>

<style>
/* 全局样式 */
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px; /* 增加顶部边距，避免内容被遮挡 */
}
</style>