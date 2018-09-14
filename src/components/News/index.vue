<template>
  <div class="news">
    <h3 class="news__title">News</h3>
    <div class="news__card news__card--size--3" v-for="(news, index) in news" :key="index">
      <img :src="news.image" :alt="news.alt" />
      <h2 v-on:click="handleTitleClick(news.id)" class="news__card_title">{{news.title}}</h2>
      <p class="news__card_overview">{{news.description}}</p>
    </div>
  </div>
</template>

<script>

import image from '@/assets/dummy-image.jpeg'

export default {
  name: 'News',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      news: [
        {
          id: '1',
          title: 'Judul',
          description: 'Desc',
          image: image,
          alt: 'News Image'
        },
        {
          id: '2',
          title: 'Judul 2',
          description: 'Desc 2',
          image: image,
          alt: 'News Image'
        },
        {
          id: '3',
          title: 'Judul 3',
          description: 'Desc 3',
          image: image,
          alt: 'News Image'
        },
        {
          id: '4',
          title: 'Judul 4',
          description: 'Desc 4',
          image: image,
          alt: 'News Image'
        }
      ]
    }
  },
  methods: {
    handleTitleClick: function (id) {
      // `this` inside methods points to the Vue instance
      this.$router.push({path: '/news-detail', query: {content_id: id}})
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->

<style lang="scss" scoped>

  .news{
    padding: 10px;
    display: grid | inline-grid;
  }

  .news__card--size--3{
    width: 25%;
    float: left;
  }

</style>

<!--

<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>

-->
