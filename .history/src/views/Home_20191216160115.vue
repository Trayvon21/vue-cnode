<template>
  <div class="bgcolor">
    <el-container>
      <!-- 顶部 -->
      <el-header>
        <Tops />
      </el-header>
      <!-- 内容 -->
      <el-container class="main">
        <el-main>
          <!-- 列表部分 -->
          <router-view />
        </el-main>
        <!-- 侧边栏 -->
        <el-aside class="aside">
          <Aside />
        </el-aside>
      </el-container>
      <!-- 底部 -->
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
  line-height: 160px;
}
.el-aside {
  color: #333;
  width: 270px;
}
.main {
  width: 90%;
  margin: 20px auto;
}
.el-footer {
  color: #333;
  background: white;
}
</style>