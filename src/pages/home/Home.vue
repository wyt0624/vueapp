<template>
    <div>
      <home-header></home-header>
      <home-swiper :list='swiperList'></home-swiper>
      <home-icons :list='iconList'></home-icons>
      <home-recommend :list='recommendList'></home-recommend>
      <home-weekend :list='weekendList'></home-weekend>
    </div>
</template>
<script>
import HomeHeader from './conponents/Header'
import HomeSwiper from './conponents/Swiper'
import HomeIcons from './conponents/Icon'
import HomeRecommend from './conponents/Recommend'
import HomeWeekend from './conponents/Weekend'
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
  data() {
    return {
      iconList: [],
      recommendList: [],
      weekendList: [],
      swiperList: []
    }
  },
  methods: {
    getHomeInfo() {
      axios.get('/api/index.json')
        .then(this.getHomeInfoSucc)
    },
    getHomeInfoSucc (res) {
      res = res.data;
      const data = res.data;
      console.log(data);
      this.iconList = data.iconList;
      this.recommendList = data.recommendList;
      this.weekendList = data.weekendList;
      this.swiperList = data.swiperList;
    }
  },
  mounted () {
    this.getHomeInfo(); 
  }
}
</script>
<style>

</style>
