<template>
  <div>
    <h1>{{title}}</h1>
  </div>
</template>

<script>
import axios from 'axios'
export default {
    name:"HomePage",
    //当你想要动态页面内容有利于SEO 或者是提升渲染速度的时候，就在asyncData中发请求拿数据
    //基本用法：它会将asyncdata返回的数据融合到组件data方法返回数据一并给组件
    //调用时机：服务端渲染期间和客户端路由更新之前
    //注意事项：服务端渲染期间和客户端路由更新之前
    async asyncData(){
        const abc=await axios({
          method:'GET',
          url:'http://localhost:3000/data.json'
        })
        return abc.data
    },
    //如果是非异步数据或者普通数据，则正常的初始化到data中即可
    data(){

    }
}
</script>

<style>

</style>