<script setup>
import NavBar from "@/components/index/NavBar.vue";
import {ref} from 'vue';

</script>

<template>
  <div class="common-layout background">
    <el-container>
      <el-header>
        <NavBar class="navbar"/>
      </el-header>

      <el-main>
        <div class="container">
          <router-link to="/">
            <a style="text-decoration: none; color: inherit;"><h1>
              海洋智慧谷-基于深度学习的大数据海洋科研平台</h1></a>
          </router-link>

          <section id="section1">
            <h2>1. 我们是什么</h2>
            <p>
              欢迎您来到基于深度学习的多维度海洋生态环境监测平台！我们的平台是一个集成了先进技术的在线服务平台，旨在为用户提供全面、准确、实时的海洋生态环境监测与管理解决方案。</p>
            <img src="@/assets/imgs/introduce.png"
                 style="justify-content: center; display: block; width: 50%; margin-left: 10px">
          </section>
          <section id="section2">
            <h2>2. 我们提供什么</h2>
            <article>
              <h3 id="dashboard">2.1 控制台</h3>
              <p>控制台是用户登录后的首个页面，提供了以下功能：</p>
              <ul>
                <li>用户行为统计：显示用户的活动情况，包括登录次数等统计信息。</li>
                <li>存储空间使用情况：展示用户的存储空间使用情况，包括已使用空间、剩余空间等。</li>
                <li>硬件资源监测：实时监测服务器的硬件资源情况，包括CPU使用情况、内存使用情况等。</li>
              </ul>
            </article>

            <article>
              <h3 id="sea_eyes">2.2 海洋之眼</h3>
              <p>海洋之眼模块提供了对海洋环境中图片和视频的深度分析和处理功能，具体包括：
                <a href="#image" class="custom-link">图片识别</a>
                <a href="#video" class="custom-link">视频检测</a>
                <a href="#img_restruction" class="custom-link">图像重构</a>
              </p>


              <section>
                <h4 id="image">2.2.1 图片识别</h4>
                <p>
                  利用自主训练的YOLOv8模型，实现对海洋生物的目标检测功能。用户可以上传图片，系统将自动识别并标注出图片中的海洋生物，提供准确的识别结果。</p>
              </section>

              <section>
                <h4 id="video">2.2.2 视频检测</h4>
                <p>
                  基于YOLOv8模型，对海洋环境中的视频进行检测和分析。用户可以上传视频文件，系统将对视频中的目标进行检测，并在检测结果中标注出目标的位置和类别。</p>
                <img src="@/assets/imgs/yolov8.png" width="50%">
              </section>

              <section>
                <h4 id="img_restruction">2.2.3 图像重构</h4>
                <p>
                  采用Diffusion扩散模型，对海洋图像进行图像重构和锐化处理。用户可以上传需要处理的图像，系统将对图像进行优化处理，提高图像的清晰度和质量。</p>
              </section>
            </article>

            <article>
              <h3 id="llms">2.3 海洋语言模型</h3>
              <p>海洋语言模型集成了先进的自然语言处理技术，为用户提供智能化的文本处理功能，具体包括：</p>
              <ul>
                <li>文本分类与识别：对海洋相关文本进行分类和识别，快速定位所需信息。</li>
                <li>信息检索与查询：提供海量海洋数据的检索和查询服务，帮助用户快速获取所需信息。</li>
                <li>语义理解与问答：基于语义理解技术，为用户提供智能问答服务，解答用户提出的问题。</li>
              </ul>
            </article>

            <article>
              <h3 id="sea_info">2.4 海洋信息综合管理系统</h3>
              <p>海洋信息综合管理系统是一个集成海洋生态数据管理、分析和展示的综合性平台，主要包括以下子模块：</p>

              <section>
                <h4 id="img_manage">2.4.1 海洋生物图像管理</h4>
                <p>提供海洋生物图像数据的上传、存储和管理功能，支持图像识别和分析。</p>
              </section>

              <section>
                <h4 id="data_analysis">2.4.2 海洋生态研究分析</h4>
                <p>提供海洋生态环境数据的上传、分析和可视化展示，帮助用户深入研究海洋生态环境。</p>
              </section>

              <section>
                <h4 id="model">2.4.3 目标检测模型管理</h4>
                <p>管理不同版本的目标检测模型，提供模型的上传、更新和管理功能，确保模型的准确性和稳定性。</p>
              </section>
            </article>
          </section>
          <section id="section3">
            <h2>联系我们</h2>
            <p>如果您对我们的平台有任何疑问或建议，欢迎随时联系我们。您可以发送邮件至 <a href="yuchenzhou2001@163.com">yuchenzhou2001@163.com</a>，我们将尽快回复您的来信。感谢您选择使用我们的海洋生态环境监测平台！我们将竭诚为您提供优质的服务和支持。
            </p>
          </section>

        </div>


        <aside class="sidebar">
          <!-- 目录 -->
          <nav class="sidebar-nav">
            <ul>
              <li><a href="#section1">1.我们是什么</a></li>
              <li><a href="#section2">2.我们提供什么</a></li>
              <li><a href="#dashboard">2.1控制台</a></li>
              <li><a href="#sea_eyes">2.2海洋之眼</a></li>
              <li><a href="#image">2.2.1图片识别</a></li>
              <li><a href="#video">2.2.2视频检测</a></li>
              <li><a href="#img_restruction">2.2.3图像重构</a></li>
              <li><a href="#llms">2.3海洋语言模型</a></li>
              <li><a href="#sea_info">2.4海洋信息综合管理系统</a></li>
              <li><a href="#img_manage">2.4.1海洋生物图像管理</a></li>
              <li><a href="#data_analysis">2.4.2海洋生态研究管理</a></li>
              <li><a href="#model">2.4.3目标检测模型管理</a></li>
              <li><a href="#section3">3.联系我们</a></li>
            </ul>
          </nav>
        </aside>


      </el-main>
    </el-container>
  </div>
</template>

<style scoped>
.navbar {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
}


/* 侧边栏样式 */
.sidebar {
  background-color: rgba(255, 255, 255, 0.9); /* 设置背景颜色为白色，透明度为0.9 */
  padding: 5px; /* 设置内边距 */
  position: fixed; /* 将侧边栏固定定位 */
  top: 100px; /* 设置距离顶部的距离 */
  right: 10px; /* 设置距离右侧的距离 */
  width: 200px; /* 设置宽度 */
  z-index: 1; /* 确保侧边栏在顶部导航栏下方 */
  overflow-y: auto; /* 添加垂直滚动条 */
  height: 550px;
  border-radius: 10px; /* 添加圆角 */
  box-shadow: 0 0 20px rgba(0, 0, 0, 0.1); /* 添加阴影效果 */
}

.sidebar-nav {
  margin: 0;
  padding: 0;
  list-style-type: none;
}

.sidebar-nav li {
  margin-bottom: 10px;
}

.sidebar-nav a {
  text-decoration: none;
  color: #333;
}

.sidebar-nav a:hover {
  color: #007bff;
}

.container {
    padding: 10px;
    width: 1000px;
    margin-top: 50px;
    margin-left: 30px;
    box-shadow: 0 0 20px rgba(0, 0, 0, 0.1); /* 添加阴影效果 */
    border-radius: 10px; /* 添加圆角 */
    background-color: rgba(25, 250, 250, 0.9); /* 设置背景颜色为白色，透明度为0.9 */
    color: black;
    font-family: sans-serif;
}

.custom-link {
    color: blue; /* 设置链接文字颜色为蓝色 */
    text-decoration: none; /* 去除链接的下划线 */
    margin-right: 10px; /* 设置链接之间的右边距 */
}

.custom-link:hover {
    text-decoration: underline; /* 鼠标悬停时显示下划线 */
}

</style>
