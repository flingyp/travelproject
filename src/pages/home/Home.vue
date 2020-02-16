<template>
  <div>
    <!-- 主页-Header -->
    <home-header></home-header>
    <!-- 主页-Swiper -->
    <home-swiper></home-swiper>
  </div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper
  }
}
</script>

<style>
</style>
