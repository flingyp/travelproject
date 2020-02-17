<template>
  <div>
    <!-- 主页-Header -->
    <home-header></home-header>
    <!-- 主页-Swiper -->
    <home-swiper></home-swiper>
    <!-- 主页-Icons -->
    <home-icons></home-icons>
    <!-- 主页-Recommend -->
    <home-recommend></home-recommend>
    <!-- 主页-Weekend -->
    <home-weekend></home-weekend>
  </div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icons'
import HomeRecommend from './components/Recommend'
import HomeWeekend from './components/Weekend'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeRecommend,
    HomeWeekend
  }
}
</script>

<style>
</style>
