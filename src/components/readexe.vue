<template>
    <div>
<topnavi :info="pInfo5"></topnavi>
<leftbar :info2="pInfo6"></leftbar>

<div class="container">
<div><el-button type="text" icon="el-icon-refresh" style="position: relative;left: 440px;">换一批</el-button></div>
 <!--:offset="index > 0 ? 3 : 0"-->
    <el-row v-for="i in 2" :key="i">
  <el-col :span="8" v-for="(o, index) in 3" :key="o" style="padding: 20px;">
    <el-card :body-style="{ padding: '10px'}" >
      <img src="https://shadow.elemecdn.com/app/element/hamburger.9cf7b091-55e9-11e9-a976-7f4d0b07eef6.png" class="image">
      <div style="padding: 14px;">
        <span>文章名</span>
        <div class="bottom clearfix">
          <time class="time">{{ currentDate }}</time>
          <el-button type="text" class="button">进入阅读</el-button>
        </div>
      </div>
    </el-card>
  </el-col>
</el-row>







</div>
    </div>
</template>

<script>
import topnavi from './topnavi.vue'
import leftbar from './leftbar.vue'

export default {
  name: 'readexe',
  components: {
    topnavi,
    leftbar
  },


  data: function(){
        return {
        pInfo5:'3-1-3',
        pInfo6:'1-3',
        loading: true,
        currentDate: new Date(),
        lists: [],
        }
    },

    mounted() {
      this.loading = false
      this.lists = [
        {
          imgUrl:
            'https://fuss10.elemecdn.com/a/3f/3302e58f9a181d2509f3dc0fa68b0jpeg.jpeg',
          name: '鹿',
        },
        {
          imgUrl:
            'https://fuss10.elemecdn.com/1/34/19aa98b1fcb2781c4fba33d850549jpeg.jpeg',
          name: '马',
        },
        {
          imgUrl:
            'https://fuss10.elemecdn.com/0/6f/e35ff375812e6b0020b6b4e8f9583jpeg.jpeg',
          name: '山狮',
        },
      ]
    },
    methods: {
      setLoading() {
        this.loading = true
        setTimeout(() => (this.loading = false), 2000)
      },
    },





}

</script>


<style>
 .time {
    font-size: 13px;
    color: #999;
  }
  
  .bottom {
    margin-top: 13px;
    line-height: 12px;
  }

  .button {
    padding: 0px;
    float: right;
  }

  .image {
    width: 80%;
    display: block;
    position: relative;
    left: 33px;
    top: 10px;
  }

  .clearfix:before,
  .clearfix:after {
      display: table;
      content: "";
  }
  
  .clearfix:after {
      clear: both
  }

</style>