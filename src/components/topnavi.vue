//顶部导航栏
<template>
<div class="whole">
    <el-menu
  :default-active="activeIndex"
  class="start"
  mode="horizontal"
  @select="handleSelect"
  background-color="#04364a"
  text-color="#fff"
  active-text-color="#ffd04b">
  <el-menu-item index="1"><i class="fa fa-map-marker"></i>首页导航</el-menu-item>
  <el-menu-item index="2" ><i class="fa fa-comments-o"></i>交流专区</el-menu-item>
  <el-submenu index="3">
    <template slot="title"><i class="fa fa-mortar-board" style="margin-right: 5px;"></i>学习专区</template>
    
    <el-submenu index="3-1">
      <template slot="title">阅读练习</template>
      <el-menu-item index="3-1-1">四级英语</el-menu-item>
      <el-menu-item index="3-1-2">六级英语</el-menu-item>
      <el-menu-item index="3-1-3">外刊阅读</el-menu-item>
    </el-submenu>

    <el-submenu index="3-2">
      <template slot="title">口语练习</template>
      <el-menu-item index="3-2-1">视频跟练</el-menu-item>
      <el-menu-item index="3-2-2">A I 对话</el-menu-item>
    </el-submenu>
    <el-menu-item index="3-3"><i class="fa fa-pencil-square-o"></i>作文批改</el-menu-item>
    <el-menu-item index="3-4"><i class="fa fa-etsy" style="margin-right: 10px;"></i>单词识记</el-menu-item>
  </el-submenu>
  <el-menu-item index="4"><a href="https://www.ele.me" target="_blank" style="text-decoration:none;"><i class="fa fa-paper-plane-o" style="margin-right: 5px;"></i>学情追踪</a></el-menu-item>
</el-menu>

</div>
</template>

<script>
export default {

  props: {
    info: {
      type: String,
      required: true
    }
  },

  mounted() {
    this.activeIndex = this.info;
  },


    data() {
      return {
        activeIndex: '1'
      };
    },
    methods: {
      handleSelect(key, keyPath) {
        console.log(key, keyPath);
      }
    }
}
</script>

<style>
.whole{
    margin-top: 90px;
    background-color: #04364a;
}
.start{
    margin-left: 220px;
    font-family:Arial,Helvetica,sans-serif;
    font-size:100px;
}


</style>