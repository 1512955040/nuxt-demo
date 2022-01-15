<template>
  <h1>User Page</h1>
</template>

<script>
export default {
    name:'UserPage',
    created(){
        //创建下划线_id.vue （备注：必须叫_id.vue） 比如user/_id.vue 访问浏览器则可传递参数 user/3
        console.log(this.$route.params.id)
    }
}
</script>

<style>

</style>