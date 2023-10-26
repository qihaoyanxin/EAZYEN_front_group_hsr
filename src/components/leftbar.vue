//左侧导航栏
<template>
    <div class="whole2">
        <el-menu
      :default-active="activeIndex2"
      class="el-menu-vertical-demo"
      :default-openeds="openeds"
      background-color="#176b87"
      text-color="#fff"
      active-text-color="#ffd04b">
      <el-submenu index="1">
        <template slot="title">
          <i class="el-icon-document" style="margin-right: 5px;"></i>
          <span>阅读练习</span>
        </template>
          <el-menu-item index="1-1" style="font-size: 12.5px;">四级英语</el-menu-item>
          <el-menu-item index="1-2" style="font-size: 12.5px;">六级英语</el-menu-item>
          <el-menu-item index="1-3" style="font-size: 12.5px;">外刊阅读</el-menu-item> 
      </el-submenu>

      <el-submenu index="2">
        <template slot="title">
          <i class="fa fa-commenting" style="margin-right: 7px;"></i>
          <span>口语练习</span>
        </template>
          <el-menu-item index="2-1" style="font-size: 12.5px;">视频跟练</el-menu-item>
          <el-menu-item index="2-2" style="font-size: 12.5px;">A I 对话</el-menu-item>
      </el-submenu>

      <el-menu-item index="3">
        <span slot="title"><i class="fa fa-pencil-square-o" style="margin-right: 7px;"></i>作文批改</span>
      </el-menu-item>
      <el-menu-item index="4">
        <span slot="title"><i class="fa fa-etsy" style="margin-right: 10px;"></i>单词识记</span>
      </el-menu-item>
    </el-menu>
 
    </div>
</template>

<script>
export default {

  props: {
    info2: {
      type: String,
      required: true
    }
  },

  mounted() {
    this.activeIndex2 = this.info2;
  },


    data() {
      return {
        activeIndex2: '1',
        openeds: ['1','2'],//默认展开导航栏
      };
    },
    methods: {
      
    }
}
</script>

<style>
.whole2{
    width: 200px;
    margin-top: 20px;
    margin-left: 20px;
}
</style>