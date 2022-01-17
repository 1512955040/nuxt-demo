<template>
  <div>
      <h1>article page</h1>
      <div>
          {{article.body}}
          <!-- <div v-for="(item,index) in dataArray">
              <div v-if="item.id==$route.params.id">{{ item.body }}</div>
          </div> -->
      </div>
  </div>
</template>

<script>
import axios from 'axios'
export default {
    name:'ArticlePage',
    async asyncData(context){
        const { data } = await axios({
            method: 'GET',
            url: 'http://localhost:3000/data.json'
        })
        const id=context.params.id
        return{
            article:data.posts.find(item=>item.id==id) 
        } 
    },
    // data(){
    //     return{
    //         dataArray:[]
    //     }
    // },
    methods:{
        // aaa(){
        //     axios({
        //         method: 'GET',
        //         url: 'http://localhost:3000/data.json'
        //     }).then(data=>{
        //         // console.log(data)
        //         data.data.posts.forEach(element => {
        //             // console.log(element)
        //             this.dataArray.push(element)
                    
        //         });
                
        //     })
        // }
    },
    created(){
        //console.log(this.$route.params.id)
        // this.aaa()
    }
}
</script>

<style>

</style>