<template>
  <div class="bgcolor">
    <el-container>
      <!-- 顶部 Tops -->
      <el-header>
        <Tops />
      </el-header>
      <!-- 中间 -->
      <el-container class="middle">
        <el-main class="main">
          <!-- 列表部分 main.vue与login.vue -->
          <router-view />
        </el-main>
        <!-- 侧边栏 Aside -->
        <el-aside class="aside">
          <Aside />
        </el-aside>
      </el-container>
      <!-- 底部 Footer -->
      <el-footer>
        <Footer />
      </el-footer>
    </el-container>
  </div>
</template>

<script>
import Aside from "../components/index/Aside";
import Tops from "../components/index/Tops";
import Footer from "../components/index/Footer";
export default {
  data() {
    return {};
  },
  components: {
    Aside,
    Tops,
    Footer
  },
  methods: {},
  mounted() {
    this.$store.dispatch("getList");
  },
  watch: {},
  computed: {}
};
</script>

<style scoped lang='scss'>
.bgcolor {
  background-color: #e9eef3;
}
.el-header {
  background-color: #333;
  color: white;
}
.el-main {
  background-color: #e9eef3;
  color: #333;
}
.el-aside {
  color: #333;
  width: 270px;
}
.middle {
  width: 90%;
  margin: 20px auto;
}
.el-footer {
  color: #333;
  background: white;
}
</style>