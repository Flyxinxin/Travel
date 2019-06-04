<template>
  <div>
    <home-header></home-header>
    <home-swiper></home-swiper>
    <home-icons></home-icons>
    <home-recommend></home-recommend>
    <home-weekend></home-weekend>
  </div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/icons'
import HomeRecommend from './components/Recommend'
import HomeWeekend from './components/Weekend'
import axios from 'axios'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeRecommend,
    HomeWeekend
  },
  methods: {
    getHomeInfo(){  //获取ajax数据then返回的是promise对象
      axios.get('/api/index.json').then(this.getHomeInfoSucc);
      console.log("axios get request start...");
    },
    getHomeInfoSucc(res){
      console.log(res);
    }
  },
  mounted() {
    this.getHomeInfo();
  },
  
}
</script>

<style>

</style>
