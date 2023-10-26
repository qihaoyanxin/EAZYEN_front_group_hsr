<template>
    <div>
<topnavi :info="pInfo1"></topnavi>
<leftbar :info2="pInfo2"></leftbar>

<div class="container">
<!---->
  <el-row v-for="i in 2" :key="i">
<el-col v-for="item in lists" :key="item.name" style="padding: 20px;" :span="8">
  <el-card 
    class="box-card" 
    :body-style="{ padding: '0px'}"
   >
    <a :href="item.videoUrl"><img :src="item.imgUrl" class="video-pic"></a>
  </el-card>
  <div class="box-text">{{ item.videotext }}</div>
 </el-col> 
</el-row>
</div>


    </div>
</template>

<script>

import topnavi from './topnavi.vue'
import leftbar from './leftbar.vue'


export default {
  name: 'oralprac',
  components: {
    topnavi,
    leftbar
  },

  data: function(){
    return{

        pInfo1:'3-2-1',
        pInfo2:'2-1',
        lists: [
        {
          imgUrl:  require("@/assets/EAZYEN.png"),
          videoUrl:'https://www.bilibili.com/video/BV1BV4y1o7jp/?spm_id_from=333.337.search-card.all.click',
          name: 'video1',
          videotext:"视频1内容"
        },
        {
          imgUrl:  require("@/assets/logo.png"),
          videoUrl:'https://www.bilibili.com/video/BV1BV4y1o7jp/?spm_id_from=333.337.search-card.all.click',
          name: 'video2',
          videotext:"视频2内容"
        },
        {
          imgUrl:  'https://fuss10.elemecdn.com/0/6f/e35ff375812e6b0020b6b4e8f9583jpeg.jpeg',
          videoUrl:'https://www.bilibili.com/video/BV1BV4y1o7jp/?spm_id_from=333.337.search-card.all.click',
          name: 'video3',
          videotext:"视频3内容"
        },
        ],
    }
  },



  /*mounted() {
      this.lists = [
        {
          imgUrl:
            '../assets/EAZYEN.png',
          name: 'vedio1',
          vediotext:"视频1内容"
        },
        {
          imgUrl:
            'https://fuss10.elemecdn.com/1/34/19aa98b1fcb2781c4fba33d850549jpeg.jpeg',
          name: 'vedio2',
          vediotext:"视频2内容"
        },
        {
          imgUrl:
            'https://fuss10.elemecdn.com/0/6f/e35ff375812e6b0020b6b4e8f9583jpeg.jpeg',
          name: 'vedio3',
          vediotext:"视频3内容"
        },
      ]
    },*/

}
</script>


<style>
 .box-card {
    width: 270px;
    height: 150px;
  }

  .box-text{
    width: 270px;
    height: 50px;
    text-align: left;
  }

.video-pic{
    width: 270px;
    height: 150px;
    size: 30%;
}

</style>