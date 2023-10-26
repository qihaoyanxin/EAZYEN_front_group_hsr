//作文批改展示页面
<template>
  <div>
<topnavi :info="pInfo1"></topnavi>
<leftbar :info2="pInfo2"></leftbar>
<!--容器-->
<div class="container">

<div id="essaydemand" class="text">
  <div style="float: left;">选择你的批改需求:</div>
  <br><br>
  <el-checkbox-group v-model="checkList" style="float: left;">
    <el-checkbox label="检查谓语动词"></el-checkbox>
    <el-checkbox label="检查语态一致"></el-checkbox>
    <el-checkbox label="检查单词拼写"></el-checkbox>
    <el-checkbox label="词汇量"></el-checkbox>
    <el-checkbox label="上下文衔接"></el-checkbox>
  </el-checkbox-group>
</div>  
  
  <!--要求文本框
 <div class="text" id="">
  
  <el-input
  type="textarea"
  :rows="4"
  placeholder="请输入需求"
  v-model="textarea">
</el-input></div>-->


  <!--内容文本框-->
    <div class="text" id="essaycontent">
      <div style="height:25px;float: left;width: 800px;background-color: #176b87;color: #FFF;text-align: left;font-size: 13px;text-indent: 5px;">提交你的作文</div>
<el-input
  type="textarea"
  :rows="18"
  placeholder="请输入作文"
  v-model="textarea">
</el-input></div>


<!--提交按钮-->
<el-button
style="background-color: #64CCC5;"
class="btton"
@click="Submit"
>
提交作文</el-button>





</div>
  </div>  
</template>

<script>
import topnavi from './topnavi.vue'
import leftbar from './leftbar.vue'
export default {
  name: 'Essaycorrection',
  components: {
    topnavi,
    leftbar
  },
  data: function(){
        return {
        textarea: '',
        checkList: [],
        pInfo1:'3-3',
        pInfo2:'3'
        }
    },

  methods:{
    Submit(){

    },
  },
}
</script>

<style>
.text{
  width: 800px;
  padding: 25px;
}

.btton{
  margin-left: 550px;
}

.container{
  width: 1000px;
  height: 700px;
  position: absolute;
  left: 300px;
  top: 170px;
}

.selection{
  float: left;

}
</style>