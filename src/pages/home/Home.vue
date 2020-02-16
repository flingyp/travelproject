<template>
  <div>
    <!-- 主页-Header -->
    <home-header></home-header>
    <!-- 主页-Swiper -->
    <home-swiper></home-swiper>
    <!-- 主页-Icons -->
    <home-icons></home-icons>
  </div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icons'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons
  }
}
</script>

<style>
</style>
