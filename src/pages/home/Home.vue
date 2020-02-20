<template>
  <div>
    <!-- 主页-Header -->
    <home-header></home-header>
    <!-- 主页-Swiper -->
    <home-swiper :list="swiperList"></home-swiper>
    <!-- 主页-Icons -->
    <home-icons :list="iconList"></home-icons>
    <!-- 主页-Recommend -->
    <home-recommend :list="recommendList"></home-recommend>
    <!-- 主页-Weekend -->
    <home-weekend :list="weekendList"></home-weekend>
  </div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icons'
import HomeRecommend from './components/Recommend'
import HomeWeekend from './components/Weekend'
import axios from 'axios'
import { mapState } from 'vuex'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeRecommend,
    HomeWeekend
  },
  data () {
    return {
      lastCity: '',
      swiperList: [],
      iconList: [],
      recommendList: [],
      weekendList: []
    }
  },
  computed: {
    ...mapState(['city'])
  },
  methods: {
    // 用于发送请求
    getHomeInfo () {
      axios.get('/api/index.json?city=' + this.city).then(this.getHomeInfoSucc)
    },
    // 用于获取数据
    getHomeInfoSucc (res) {
      res = res.data
      if (res.ret && res.data) {
        const data = res.data
        this.swiperList = data.swiperList
        this.iconList = data.iconList
        this.recommendList = data.recommendList
        this.weekendList = data.weekendList
      }
      // console.log(res)
    }
  },
  mounted () {
    this.lastCity = this.city
    // 页面挂载好后 执行这个函数 获取主页Home数据
    this.getHomeInfo()
  },
  activated() {
    if (this.lastCity !== this.city) {
      this.getHomeInfo()
    }
  }
}
</script>

<style>
</style>
