<template>
  <div id="app" >
    <img src="./assets/EAZYEN.png" alt="EAZYEN" class="logo">
    
      <oralprac></oralprac>
    
    <!--<readexe></readexe>-->
    <!--<Essaycorrection></Essaycorrection>
    <correctresult></correctresult>-->
  </div>
</template>

<script>
import readexe from './components/readexe.vue'
import Essaycorrection from './components/Essaycorrection.vue';
import correctresult from './components/correctresult.vue';
import oralprac from './components/oralprac.vue';
export default {
  name: 'App',
  components: {
    readexe,
    Essaycorrection,
    correctresult,
    oralprac

  }
}
/*import daohang from './components/daohang.vue'
import leftbar from './components/leftbar.vue'
export default {
  name: 'App',
  components: {
    daohang,
    leftbar
  }
}*/
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.logo{
  width: 400px;
  height: 220px;
  position: absolute;
  left: 10px;
  top: -65px;
}
</style>
