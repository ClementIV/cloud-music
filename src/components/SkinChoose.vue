<template>
    <div class="skin-choose">
        <el-tabs v-model="activeName" @tab-click="handleClick">
            <el-tab-pane label="主题" name="first">
                <div class="row skin-theme-margin">
                 <div class="col-sm-4 theme-hover-black" >
                     <div class="skin-theme-black skin-theme">
                         <div class="skin-theme-text">炫酷黑</div>
                     </div>
                 </div>
                 <div class="col-sm-4 theme-hover-red" >
                     <div class="skin-theme-red skin-theme">
                         <div class="skin-theme-text">官方红</div>
                     </div>
                 </div>
                 <div class="col-sm-4 theme-hover-pink" >
                     <div class="skin-theme-pink skin-theme">
                         <div class="skin-theme-text">可爱粉</div>
                     </div>
                 </div>
                </div>
                <div class="row skin-theme-margin">
                 <div class="col-sm-4 theme-hover-skyblue">
                     <div class="skin-theme-skyblue skin-theme">
                         <div class="skin-theme-text">天际蓝</div>
                     </div>
                 </div>
                 <div class="col-sm-4 theme-hover-springgreen" >
                     <div class="skin-theme-springgreen skin-theme">
                         <div class="skin-theme-text">清新绿</div>
                     </div>
                 </div>
                 <div class="col-sm-4 theme-hover-gold" >
                     <div class="skin-theme-gold skin-theme">
                         <div class="skin-theme-text">金色</div>
                     </div>
                 </div>
                </div>
            </el-tab-pane>
            <el-tab-pane label="纯色" name="second">配色选择
                <div class="row skin-theme-margin">
                    <div class="col-sm-2 theme-hover-black" >
                        <div class="skin-theme-black skin-theme-color"></div>
                    </div>
                    <div class="col-sm-2 theme-hover-red" >
                        <div class="skin-theme-red skin-theme-color"></div>
                    </div>
                    <div class="col-sm-2 theme-hover-pink" >
                        <div class="skin-theme-pink skin-theme-color"></div>
                    </div>
                    <div class="col-sm-2 theme-hover-skyblue" >
                        <div class="skin-theme-skyblue skin-theme-color"></div>
                    </div>
                    <div class="col-sm-2 theme-hover-springgreen" >
                        <div class="skin-theme-springgreen skin-theme-color"></div>
                    </div>
                    <div class="col-sm-2 theme-hover-gold" >
                        <div class="skin-theme-gold  skin-theme-color"></div>
                    </div>
                </div>
                <div class="row skin-theme-margin">
                    <div class="col-sm-2 theme-hover-black" >
                        <div class="skin-theme-black skin-theme-color"></div>
                    </div>
                    <div class="col-sm-2 theme-hover-red" >
                        <div class="skin-theme-red skin-theme-color"></div>
                    </div>
                    <div class="col-sm-2 theme-hover-pink" >
                        <div class="skin-theme-pink skin-theme-color"></div>
                    </div>
                    <div class="col-sm-2 theme-hover-skyblue" >
                        <div class="skin-theme-skyblue skin-theme-color"></div>
                    </div>
                    <div class="col-sm-2 theme-hover-springgreen" >
                        <div class="skin-theme-springgreen skin-theme-color"></div>
                    </div>
                    <div class="col-sm-2 theme-hover-gold" >
                        <div class="skin-theme-gold  skin-theme-color"></div>
                    </div>
                </div>
                自定义颜色
                <div class="row skin-theme-margin">
                    <el-color-picker v-model="color3" show-alpha></el-color-picker>
                </div>
            </el-tab-pane>

        </el-tabs>
    </div>
</template>
<script>
export default {
   data() {
     return {
       activeName: 'first',
       color3: 'rgba(19, 206, 102, 0.8)'
     };
   },
   methods: {
     handleClick(tab, event) {
       // console.log(tab, event);
     }
   }
 };
</script>
<style>

.skin-choose{
    padding: 0 15px 15px 15px;
}
.skin-theme-margin{
    margin: 5px 0px 0 5px;
}
.skin-theme-color{
    width: calc(100%);
    height: 0;
    padding-bottom:  calc(100%);
    /* background: url(../assets/music.png) no-repeat center center; */
    zoom:1;
    cursor: pointer;
    /* background-size: contain; */
    display: block;
}
.skin-theme{
   width: calc(100%);
   height: 0;
   padding-bottom:  calc(100%);
   background: url(../assets/music.png) no-repeat center center;
   zoom:1;
   cursor: pointer;
   /* background-size: contain; */
   display: block;
   /* border: 2px solid transparent; */
}
.theme-hover-black,.theme-hover-red,.theme-hover-pink,
.theme-hover-skyblue,.theme-hover-springgreen,.theme-hover-gold {
    border: 2px solid transparent;
    padding: 2px!important;
}
.theme-hover-black:hover {
    border: 2px solid #000;
}
.theme-hover-red:hover {
    border: 2px solid  #E0230E;
}
.theme-hover-pink:hover {
    border: 2px solid  #FFB6C1;
}
.theme-hover-skyblue:hover {
    border: 2px solid  #87CEEB;
}
.theme-hover-springgreen:hover {
    border: 2px  solid #3CB371;
}
.theme-hover-gold:hover {
    border: 2px  solid #FFD700;
}
.skin-theme-text{
    width: calc(100% - 4px);
    height: 22px;
    margin: 0;
    line-height: 22px;
    text-indent: 10px;
    background-color:rgba(0,0,0,0.2);
    /* margin-bottom: 0; */
    position: absolute;
    bottom: 2px;
    color: #FFF;

}
.skin-theme-black{

    background-color: #000;
}
.skin-theme-red{

    background-color: #E0230E;
}
.skin-theme-pink{

    background-color: #FFB6C1;
}
.skin-theme-skyblue{
    background-color:#87CEEB;
}
.skin-theme-springgreen{
    background-color:#3CB371;
}
.skin-theme-gold{
    background-color:#FFD700;
}
</style>
