<template>
  <div class="tables">
    <div v-for="item in list" :key="item.id" class="desc">
        <!-- 用户图标 -->
      <div>
        <div v-if="item.author.avatar_url">
          <img :src="item.author.avatar_url" alt />
        </div>
        <div v-else>
          <div></div>
        </div>
      </div>
      <!-- 访问量 -->
      <div>
          <div></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
  components: {},
  methods: {},
  mounted() {},
  watch: {},
  computed: {
    list() {
      return this.$store.state.list;
    }
  }
};
</script>

<style scoped lang='scss'>
.desc {
  width: 100%;
  background: white;
  margin-bottom: 2px;
  height: 30px;
  padding: 10px 0;
  display: flex;
}
img {
  margin-left: 20px;
  width: 30px;
  height: 30px;
}
</style>