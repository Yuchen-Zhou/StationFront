<script setup>
import SideBar from "@/components/dashboard/SideBar.vue";
import UserStorage from "@/components/dashboard/UserStorage.vue";
</script>

<template>
  <div>
    <el-container class="full-container">
      <el-aside class="sidebar"> <!-- 将样式类应用到 el-aside 元素 -->
        <SideBar/>
      </el-aside>
      <el-main>
        <img src="@/assets/imgs/dashboard.png" class="img-background">

        <UserStorage/>
      </el-main>
    </el-container>
  </div>
</template>

<style scoped>
.sidebar {
  position: fixed; /* 将侧栏固定定位 */
  top: 0; /* 距离顶部为 0 */
  left: 0; /* 将侧栏固定在页面最左侧 */
  width: 200px; /* 设置侧栏的宽度 */
  height: 100%; /* 将侧栏高度设置为 100% */
  background-color: rgba(0, 0, 0, 0.7); /* 设置侧栏背景颜色 */
  overflow-x: hidden; /* 水平溢出时隐藏内容 */
  transition: width 0.5s; /* 添加宽度过渡效果 */
  z-index: 2; /* 设置侧栏的 z-index 比顶部栏更高 */
}

.img-background {
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  width: 100%;
  overflow: hidden;
  z-index: -1;
}

</style>
