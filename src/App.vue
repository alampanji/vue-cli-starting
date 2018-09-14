<template>
  <div id="app">
    <header-menu />
    <router-view/>
  </div>
</template>

<script>

import Header from './components/Header'

export default {
  name: 'App',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  components: {
    'header-menu': Header
  }
}

</script>

<style>
body{
  margin: 0px;
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
