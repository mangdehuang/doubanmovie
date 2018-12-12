<template>
  <div class="Home">
    <el-container>
      <el-header>{{title}} 数目：{{allData.count}}</el-header>
      <Content :moviceList="moviceList"></Content>
    </el-container>
  </div>
</template>
<script>
import Content from "./Content";
export default {
  name: "Home",
  data() {
    return {
      title: "",
      moviceList: [],
      allData: {}
    };
  },
  created() {
    this.$http.get("api/v2/movie/in_theaters").then(res => {
      console.log(res.data);
      this.allData = res.data;
      this.title = res.data.title;
      this.moviceList = res.data.subjects;
    });
  },
  components: {
    Content
  }
};
</script>
<style lang="">
</style>
