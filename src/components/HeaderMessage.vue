<template>
<div>
  <el-tabs v-model="activeName2" type="card" @tab-click="handleClick" :stretch="true">
    <el-tab-pane label="私信" name="first"><message-list :items="item3"></message-list></el-tab-pane>
    <el-tab-pane label="评论" name="second"><message-list :items="item1"></message-list></el-tab-pane>
    <el-tab-pane label="@我" name="third"><message-list :items="item2" ></message-list></el-tab-pane>
    <el-tab-pane label="通知" name="fourth"><message-list :items="item2"></message-list></el-tab-pane>
  </el-tabs>
</div>
</template>
<script>
import MessageList from '@/components/MessageList'
export default{
    name:"HeaderMessage",
    data () {
      return {
       activeName2: 'first',
       item3:[
         {
           link:'https://music.163.com/#/user/home?id=31265745',
           imglink: 'https://p1.music.126.net/_PXn1ZMcbv5DNHGidQrhCQ==/1422768054399325.jpg?param=50y50',
           time: '2018年12月25日',
           userName: '许嵩',
           conment: 'MV-许嵩云村独家圣诞问候 by 许嵩'

         },
         {
           link:'https://music.163.com/#/user/home?id=31265745',
           imglink: 'https://p1.music.126.net/_PXn1ZMcbv5DNHGidQrhCQ==/1422768054399325.jpg?param=50y50',
           time: '2018年12月25日',
           userName: '许嵩',
           conment: 'MV-许嵩云村独家圣诞问候 by 许嵩'

         },
         {
           link:'https://music.163.com/#/user/home?id=94769339',
           imglink: 'http://p2.music.126.net/clP_peOAO1hRcWKSHZEGwQ==/109951163611897281.jpg?param=50y50',
           time: '2019年1月25日',
           userName: 'ClementIV',
           conment: 'MV-我的消息消息 by ClementIV'

         },
         {
           link:'https://music.163.com/#/user/home?id=94769339',
           imglink: 'http://p2.music.126.net/clP_peOAO1hRcWKSHZEGwQ==/109951163611897281.jpg?param=50y50',
           time: '2019年1月25日',
           userName: 'ClementIV',
           conment: 'MV-我的消息消息 by ClementIV'

         }

     ],
     item1:[

       {
         link:'https://music.163.com/#/user/home?id=94769339',
         imglink: 'http://p2.music.126.net/clP_peOAO1hRcWKSHZEGwQ==/109951163611897281.jpg?param=50y50',
         time: '2019年1月25日',
         userName: 'ClementIV',
         conment: 'MV-我的消息消息 by ClementIV'

       },
       {
         link:'https://music.163.com/#/user/home?id=94769339',
         imglink: 'http://p2.music.126.net/clP_peOAO1hRcWKSHZEGwQ==/109951163611897281.jpg?param=50y50',
         time: '2019年1月25日',
         userName: 'ClementIV',
         conment: 'MV-我的消息消息 by ClementIV'

       },
       {
         link:'https://music.163.com/#/user/home?id=31265745',
         imglink: 'https://p1.music.126.net/_PXn1ZMcbv5DNHGidQrhCQ==/1422768054399325.jpg?param=50y50',
         time: '2018年12月25日',
         userName: '许嵩',
         conment: 'MV-许嵩云村独家圣诞问候 by 许嵩'

       },
       {
         link:'https://music.163.com/#/user/home?id=31265745',
         imglink: 'https://p1.music.126.net/_PXn1ZMcbv5DNHGidQrhCQ==/1422768054399325.jpg?param=50y50',
         time: '2018年12月25日',
         userName: '许嵩',
         conment: 'MV-许嵩云村独家圣诞问候 by 许嵩'

       }

   ],

      item2:[

        {
          link:'https://music.163.com/#/user/home?id=94769339',
          imglink: 'http://p2.music.126.net/clP_peOAO1hRcWKSHZEGwQ==/109951163611897281.jpg?param=50y50',
          time: '2019年1月25日',
          userName: 'ClementIV',
          conment: 'MV-我的消息消息 by ClementIV'

        },
        {
          link:'https://music.163.com/#/user/home?id=94769339',
          imglink: 'http://p2.music.126.net/clP_peOAO1hRcWKSHZEGwQ==/109951163611897281.jpg?param=50y50',
          time: '2019年1月25日',
          userName: 'ClementIV',
          conment: 'MV-我的消息消息 by ClementIV'

        },
        {
          link:'https://music.163.com/#/user/home?id=31265745',
          imglink: 'https://p1.music.126.net/_PXn1ZMcbv5DNHGidQrhCQ==/1422768054399325.jpg?param=50y50',
          time: '2018年12月25日',
          userName: '许嵩',
          conment: 'MV-许嵩云村独家圣诞问候 by 许嵩'

        },
        {
          link:'https://music.163.com/#/user/home?id=31265745',
          imglink: 'https://p1.music.126.net/_PXn1ZMcbv5DNHGidQrhCQ==/1422768054399325.jpg?param=50y50',
          time: '2018年12月25日',
          userName: '许嵩',
          conment: 'MV-许嵩云村独家圣诞问候 by 许嵩'

        }

      ]
       }
    },
    components:{
        MessageList
    },
    methods: {
      handleClick(tab, event) {
       console.log(tab, event);
      }
    }
}
</script>
<style>
</style>
