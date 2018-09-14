<template>
    <div class="nav">
        <div class="nav__menu">
           <ul>
                <li v-for="(menu, index) in menuList" :key="index">
                    <router-link :to="{path: menu.path}"> {{menu.label}} </router-link>
                </li>
           </ul>
        </div>
    </div>
</template>

<script>
export default {
  name: 'Header',
  data () {
    return {
      menuList: [
        {label: 'Home', path: '/'},
        {label: 'About', path: '/about'},
        {label: 'News', path: '/news'}
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
    .nav{
        width:100%;
        height: 100px;
        background: #0097e6;
        .nav__menu{
            ul{
                margin: 0px;
                li{
                    list-style: none;
                    float: left;
                    padding: 10px;
                    a{
                        color: #ffffff;
                        text-decoration: none;
                    }
                }
            }
        }
    }
</style>
