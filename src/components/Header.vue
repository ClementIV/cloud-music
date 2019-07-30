<template>
    <div class="img">
        <div class="logo" >网易云音乐</div>
        <el-button-group class="button-arrow" >
            <el-button type="primary" icon="el-icon-arrow-left" size="mini"></el-button>
            <el-button type="primary" icon="el-icon-arrow-right" size="mini"></el-button>
        </el-button-group >
        <div class="header-content">
            <el-input name="searchInput" max ="300" min="200" class="button-input" placeholder="搜索音乐，视频，歌词，电台"  v-model="inputSearch">
                <template slot="append"><a href="javascript:void(0)" @click="doSearch"><i  class="el-icon-search"></i></a></template>
            </el-input>
        </div>
        <div >
            <span class="header-icon" v-html="iconClose"></span>
            <span v-if="!isMax" class="header-icon" @click="formMax" v-html="iconMax"></span>
            <span v-if="isMax" class="header-icon" @click="formMaxToSmall" v-html="iconNormal"></span>
            <span class="header-icon" @click="formMinus" v-html="iconMin"></span>
            <span v-if="isMax" class="header-icon" ><i  class="el-icon-min"></i></span>
            <span class="header-icon-sp" ><i  class="el-icon-sp"></i></span>
            <span class="header-icon" @click="formMinus" ><i  class="el-icon-setting"></i></span>
            <span  class="header-icon" >
              <el-popover id ="head-message" popper-class="head-message" placement="bottom" title="               " width="360" trigger="click" visible-arrow="false" style="margin:0px;">
                  <header-message></header-message>
                 <el-badge v-bind:is-dot="isMax" class="item"  slot="reference" >
                     <i  class="el-icon-message " ></i>
                 </el-badge>
              </el-popover></span>
            <span  class="header-icon" >
                <el-popover placement="bottom"  title="               " width="360"  trigger="click" visible-arrow="false" style="margin:0px;">
                    <skin-choose></skin-choose>
                    <i  class="el-icon-skin"slot="reference"  ></i>
                </el-popover>
            </span>
            <span  class="header-login" >
                <img src="../assets/userimg.jpg" class="img-circle img-login"></img>
                <el-popover placement="bottom" width="360"  trigger="click" visible-arrow="false" style="margin:0px;">
                    <skin-choose></skin-choose>
                    <div slot="reference" class="login-username "  >未登录<i class="el-icon-arrow-down el-icon--right"></i></div>
                </el-popover>
            </span>
            <div v-html="message"></div>
        </div>
    </div>
</template>
<script>
/* eslint-disable no-new */
import HelloWorld from '@/components/HelloWorld'
import HeaderMessage from '@/components/HeaderMessage'
import SkinChoose from '@/components/SkinChoose'
export default {
  name: 'PageHeader',
  data () {
    return {
      visible:false,
      inputSearch: '',
      isMax: false,
      message: '<button class="btn btn-info" onclick="headerJsObject.showDevTools();">Open Dev</button>',
      iconClose: '<i  class="el-icon-close" onclick="headerJsObject.closeForm();"></i>',
      iconMax: '<i  class="el-icon-max" onclick="headerJsObject.maxForm();"></i>',
      iconMin: '<i  class="el-icon-minus" onclick="headerJsObject.minForm();"></i>',
      iconNormal: '<i  class="el-icon-max-to-samll" onclick="headerJsObject.normalForm();"></i>',
      isSkin:false
    }
  },
  components:{
    HelloWorld,
    HeaderMessage,
    SkinChoose
    },
  methods: {
    doSearch () {
      alert(this.inputSearch)
    },
    formMax () {
      // alert('max')
      this.isMax = true
    },
    formMaxToSmall () {
      this.isMax = false
    },
    formMinus () {
      this.isMax = false
    }
  }
}
</script>
<style>
 .head-message.el-popper{
    margin-top: 5px !important;
    float: right !important;
    height: calc(100% - 118px);
}
.item {
  margin-top: 0px;
  margin-right: 5px;
}
.el-dropdown-link {
    cursor: pointer;
    color: #409EFF;
  }
.el-icon-arrow-down {
    font-size: 12px;
  }
.img-login{
    width: 28px;
    height: 28px;
    display: inline;
    border-radius: 50%;
}
.login-username{
    width:90px;
    display: inline-block;
    text-align: left;
    font-size: 14px;
    line-height: 14px;
    color: #d5d5d5;
    overflow: hidden;
}
.login-username:hover{
    color:#FFF;
}
.header-login{
    float: right;
    text-align: center;
    margin: 2px 4px;
    color:#dbdbdb;
    line-height: 32px;
    height: 32px;
    cursor:pointer;
    width:125px;
    display: inline;
}
.el-popover__title{
    margin-bottom: 30px;
}
.el-input-group__append{
    height: 24px !important;;
    line-height: 24px !important;;
    background: #a40011 !important;;
    border: 1px solid #a40011 !important;;
    color:#9b9b9b !important;;
    border-radius: 0px 13px 13px 0  !important;
    width: 26px;
    padding: 0px !important;
}
.header-content{
    min-width: 300px !important;
    max-width: 400px !important;
    display: inline-block;
    float: left;
}
.el-icon-message{
    margin-top: 3px !important;
    line-height: 1 !important;
    width: 22px !important;
    height: 22px !important;
    font-size: 20px !important;
}
.el-icon-min{
    margin-top: 5px;
    line-height: 1;
    width: 19px;
    height: 19px;
    vertical-align: baseline;
    display: inline-block;
    background: url(../assets/min.png) no-repeat;
    background-size: cover;
}
.el-icon-min:hover{
    background: url(../assets/minHover.png) no-repeat;
    background-size: cover;
}
.el-icon-skin{
    margin-top: 5px;
    line-height: 1;
    width: 19px;
    height: 19px;
    vertical-align: baseline;
    display: inline-block;
    background: url(../assets/skin.png) no-repeat;
    background-size: cover;
}
.el-icon-skin:hover{
    line-height: 1;
    width: 19px;
    height: 19px;
    background: url(../assets/skin.png) no-repeat;
    background-size: cover;
}

.el-icon-max{
    margin-top: 3px;
    line-height: 1;
    width: 22px;
    height: 22px;
    vertical-align: baseline;
    display: inline-block;
    background: url(../assets/max.png) no-repeat;
    background-size: cover;
}
.el-icon-max:hover{
    background: url(../assets/maxh.png) no-repeat;
    background-size: cover;
}
.el-icon-max-to-samll{
    margin-top: 3px;
    line-height: 1;
    width: 22px;
    height: 22px;
    vertical-align: baseline;
    display: inline-block;
    background: url(../assets/maxToSmall.png) no-repeat;
    background-size: cover;
}
.el-icon-max-to-samll:hover{
    background: url(../assets/maxToSmallh.png) no-repeat;
    background-size: cover;
}
.el-icon-sp{
    margin-top: 3px;
    line-height: 1;
    width: 22px;
    height: 22px;
    vertical-align: baseline;
    display: inline-block;
    background: url(../assets/sp.png) no-repeat;
    background-size: cover;
}
.header-icon>i:hover{

    color:#FFf;
}
.header-icon{
    float: right;
    text-align: center;
    margin: 2px 4px;
    color:#dbdbdb;
    line-height: 32px;
    height: 32px;
    cursor:pointer;
}
.header-icon-sp{
    float: right;
    text-align: center;
    margin: 2px -8px 2px -8px;
    color:#dbdbdb;
    line-height: 32px;
    height: 32px;
}
.header-icon>i{
    font-size: 20px;
}
.el-input-group__append>a {
    color: #9b9b9b !important;
}
.el-input-group__append>a:hover{
    color:#fff !important;
    font-weight: bold;
}
.img {
    padding-top:  5px;
    height: 35px;
    line-height: 35px;
    /* display: inline; */
}
.el-input__icon{
    line-height: 26px !important;;
}
[name="searchInput"]{
    height: 26px !important;;
    line-height: 26px !important;;
    background: #a40011 !important;;
    border: 1px solid #a40011 !important;;
    color:#9b9b9b !important;;
    border-radius: 13px 0 0 13px !important;;
}
.button-arrow{
    margin: 5px 5px;
    float: left;
    text-align: center;
    line-height: 25px;
    height:25px;
    width: 100px!important;

}
.button-input{
    margin: 5px 5px;
    float: left;
    text-align: center;
    line-height: 26px !important;
    height:26px !important;
    width: 255px !important;
}
.logo{
    float: left;
    width: 183px;
    height:45 px;
    text-indent: -9999px;
    background:  url(../assets/topbar.png);
    background-size:cover;
    background-position: 0px -10px;
 }
</style>
