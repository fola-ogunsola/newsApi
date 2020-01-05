<template>
  <div class="home">
    <newsApi/>
  </div>
  </template>

<script>
// @ is an alias to /src

import newsApi from '@/components/newsApi.vue'
export default {
  name: 'home',
  components: {
    newsApi
  }
}


</script>
