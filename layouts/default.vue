<template>
    <div>
        <!-- 目的是设置公共部分Layout组件，是一个更简便的嵌套路由，公共部分可以设置在这块 -->
        <h1>layouts/default.vue</h1>
        <!-- 页面出口，类似于子路由出口 -->
        <nuxt/>    
    </div>
</template>

<script>
export default {
    name:'LayoutDefault'
}
</script>

<style>

</style>