<template>
<div>
    <h2>Country News</h2>
    <div v-for="(items,index) in newsApi" :key="index">
      <h3>{{items.title}}</h3>
      <h6>{{items.url}}</h6>
      <img :src= 'items.urlToImage'>
    </div>
</div>
</template>
<script>
export default{
    data(){
        return {
           newsApi: []
        }
    },
    mounted(){
        this.$http.get('https://newsapi.org/v2/top-headlines?country=us&apiKey=56c2b2faa1014003b5703fbfdd5d2830')
        .then(response => {
            this.newsApi = response.data.articles;
        })
    }
}
</script>