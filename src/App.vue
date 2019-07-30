<template>
  <div id="app" class="is-component">
        <div class="headerWrapper">
          <el-header style="height:45px;">
            <page-header></page-header>
          </el-header>
        </div>
      <div  class="main-cnt">
      <el-scrollbar class="page-scrollbar">
      <el-container>
        <!-- <el-scrollbar > -->
        <el-aside width="220px">Aside</el-aside>
        <!-- </el-scrollbar> -->
        <!-- <el-scrollbar > -->
        <el-main>
            <!-- <img src="./assets/logo.png"> -->
            <router-view/>
        </el-main>
        <!-- </el-scrollbar> -->
      </el-container>
      </el-scrollbar>
    </div>
    <div class="footerWrapper">
    <el-footer style="height:50px;">Footer</el-footer>
    </div>
  </div>
</template>

<script>
import PageHeader from '@/components/Header'
// import CloseForm from '@/formJs/header'
export default {
  name: 'App',
  data () {
    return {
    }
  },
  components: {
    PageHeader
  }
}
</script>

<style>
.headerWrapper{
    position: fixed;
    width: 100%;
    left: 0;
    top: 0;
    z-index: 1500;
    height: 45px;
}
.footerWrapper{
    position: fixed;
    width: 100%;
    left: 0;
    bottom: 0;
    z-index: 1500;
    height: 50px;
}
.page-scrollbar{
    height: calc(100% - 45px);
    margin-top: 45px;
}
.main-cnt{
    padding: 0;
    box-sizing: border-box;
    height:  1000px;
    margin-bottom: 50px;

}
.el-scrollbar__wrap{
    overflow: scroll;
  overflow-x:auto
}
.el-scrollbar{
    width: 100%;
}
.el-row {
    margin-bottom: 20px;
    &:last-child {
      margin-bottom: 0;
  };
    width: 100%;
  }
.el-header {
  position: relative;
   border-bottom: 1px solid #a40011;
   background-color: #E0230E;
   color: #fff;
   text-align: center;
   line-height: 45px;
 }
 .page-component__scroll {
}
 #app.is-component .main-cnt {
    padding: 0;
    margin-top: 0;
    height: 100% !important;
    /* overflow-y: scroll; */
    min-height: auto;
}
 .el-footer {
   border-top: 1px solid #d3d3d3;
   background-color: #F6F6F6;
   color: #333;
   text-align: center;
   line-height: 50px;
 }
 .el-aside {
   /* margin-top: 45px; */
   background-color: #f5f5f5;
   color: #333;
   text-align: center;
   line-height: 200px;
   border-right: 1px solid #d3d3d3;
   margin-bottom: 50px;
 }

 .el-main {
   /* margin-top: 45px; */
   /* overflow-y: hidden; */
   background-color: #F8F8FB;
   color: #333;
   text-align: center;
   line-height: 160px;
   margin-bottom: 50px;
   height: calc(100%-45px);
   min-height:auto;
 }

 body > .el-container {
   margin-bottom: 40px;

 }
 body.is-component {
   /* overflow: hidden; */
}
 body{
     margin: 0px !important;
     height: 100%;
     overflow: hidden;
 }
 .el-container:nth-child(5) .el-aside,
 .el-container:nth-child(6) .el-aside {
   line-height: 260px;
 }

 .el-container:nth-child(7) .el-aside {
   line-height: 320px;
 }
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  /* margin-top: 60px; */
}
#app.is-component {
    overflow-y: hidden;
    height: 100%;
}
html, body {
    margin: 0;
    padding: 0;
    height: 100%;
    font-family: 'Helvetica Neue',Helvetica,'PingFang SC','Hiragino Sans GB','Microsoft YaHei',SimSun,sans-serif;
    font-weight: 400;
    -webkit-font-smoothing: antialiased;
}
</style>
