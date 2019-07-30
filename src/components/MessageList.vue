<template>
    <div >
    <ul class="list-group">
      <li class="list-group-item" v-for ="item in  items">
          <div class="ava f-pr">
              <a :href="item.link">
                 <img :src="item.imglink"></img>
              </a>
          </div>
          <div class="cont">
              <div class="sec1">
                  <div class="time">{{item.time}}</div>
                  <div class="mn"><a class="f-fs1" :href="item.link">{{item.userName}}</a></div>
              </div>
              <div class="sec2 sec2-1">
                <p class="f-thide">{{item.conment}}</p>
              </div>
          </div>
      </li>
      <!-- <li class="list-group-item">Dapibus ac facilisis in</li>
      <li class="list-group-item">Morbi leo risus</li>
      <li class="list-group-item">Porta ac consectetur ac</li>
      <li class="list-group-item">Vestibulum at eros</li> -->
    </ul>
    </div>
</template>
<script>
import '@/../node_modules/bootstrap/dist/css/bootstrap.min.css'
import '@/../node_modules/bootstrap/dist/js/bootstrap.min.js'

export default {
    props:{
         items:Array
    },
    data () {

        return {


        }
    }
}
</script>
<style>
.ava img {
    width: 50px;
    height: 50px;
    border-radius: 50%;
}
.ava {
    float: left;
    width: 40px;
    height: 40px;
    margin-right: -100px;
}
.el-popover{
    padding: 0;
}
.cont {
    margin-left: 70px;
    line-height: 21px;
}
.list-group-item{
    border: 1px !important;
}
.list-group-item:hover{
    background:#f5f5f5 !important;
}
.cont .time {
    float: right;
    color: #999;
    font-family: Tahoma, Geneva, sans-serif;
}
.f-fs1 {
    font-size: 14px;
    color:#000;
    font-weight: bolder;
}
.sec2-1 p {
    margin-top:5px;
    width: 90%;
}
.f-thide {
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
    word-wrap: normal;
}
</style>
