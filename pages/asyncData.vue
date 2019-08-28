<template>
    <div>
        <h1>姓名:{{info.name}}</h1>
        <h2>age:{{info.age}}</h2>
        <h1>intesting:{{info.intesting}}</h1>
    </div>
</template>

<script>
import axios from 'axios'
export default {
    data() {
        return {
            name:"hello world"
        }
    },
    //promise 
    // asyncData(){
    //     return axios.get('https://api.myjson.com/bins/sku87')
    //     .then((res)=>{
    //         return {info:res.data}
    //     })
    // }

    //asnyc
    async asyncData(){
        let {data} = await axios.get('https://api.myjson.com/bins/sku87')
        return {info : data}
    }
}
</script>