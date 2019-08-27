<template>
    <div>
        <h2>News-content</h2>
        <p>NewsId:{{$route.params.id}}</p>
        <ul>
            <li><a href="/">HOME</a></li>
            <li><nuxt-link :to="{name:'news-id',params:{id:123}}">news-1</nuxt-link></li>
            <li><a href="/news/456">news-2</a></li>
        </ul>
    </div>
</template>
<script>
export default {
    transition:'test'//进去news路由时的动画 名字与css中的test相同
}
</script>