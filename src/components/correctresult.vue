<template>
    <div>
        <topnavi :info="pInfo1"></topnavi>
        <leftbar :info2="pInfo2"></leftbar>
<div class="container">
    <div><el-button style="float: left;background-color: #176b87;color: #FFF;">返回</el-button></div>
<!--进度条评分域-->
<div style="position: relative;left: 100px;top: 40px;">
    <!--评分圈-->
<el-progress type="circle" :width="200" :percentage="25" style="float: left;padding-right: 50px;"></el-progress>   
 <div style="height: 172px;width: 80px;float: left;">
    <p>词汇：</p>
    <p>句子：</p>
    <p>篇章结构：</p>
    <p>内容相关：</p>
</div>
    <!--进度条-->
<div class="progress">
<el-progress :text-inside="true" :stroke-width="26" :percentage="70" class="innerprogress"></el-progress>
<el-progress :text-inside="true" :stroke-width="24" :percentage="100" status="success" class="innerprogress"></el-progress>
<el-progress :text-inside="true" :stroke-width="22" :percentage="80" status="warning" class="innerprogress"></el-progress>
<el-progress :text-inside="true" :stroke-width="20" :percentage="50" status="exception" class="innerprogress"></el-progress>
</div></div><!--评分域-->
<br>

<!--具体批改内容域-->
<div class="container2">
<div style="text-align: left; border-style: outset;background-color: #176b87;color: #FFF;">按句点评：</div>
<br><br>
    <div style="text-align: left;">青春是一个短暂的美梦, 当你醒来时, 它早已消失无踪</div>
    <el-divider></el-divider>
    <div style="text-align: left;">少量的邪恶足以抵消全部高贵的品质, 害得人声名狼藉</div>
    <el-divider></el-divider>
    <div style="text-align: left;">少量的邪恶足以抵消全部高贵的品质, 害得人声名狼藉</div>
    <el-divider></el-divider>

</div>

</div>
    </div>
</template>

<script>
import topnavi from './topnavi.vue'
import leftbar from './leftbar.vue'
export default {
    name:'correctresult',
    components: {
    topnavi,
    leftbar

  },


  data:function(){
    return{
        pInfo1:'3-3',
        pInfo2:'3'
    }

  }

}
</script>

<style>
.innerprogress{

    padding: 10px;
}

.progress{
    width: 400px;
    float: left;

}

.container2{
  width: 1000px;
  height: 700px;
  position: absolute;
  top: 300px;
  border-style: outset;
}

p{
    /*position: relative;
    top: 5px;*/
    
    padding-bottom: 5px;
}



</style>