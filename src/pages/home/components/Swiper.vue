<template>
  <div class="wrapper">
    <swiper :options="swiperOption" v-if="showSwiper">
      <swiper-slide v-for="item of list" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl" alt />
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  props: {
    list: Array
  },
  data() {
    return {
      // 轮播图选项配置
      swiperOption: {
        // 显示小点
        pagination: '.swiper-pagination',
        // 循坏播放
        loop: true,
        // 自动播放时长
        autoplay: 2000,
        // 移动速度
        speed: 1000
      }
    }
  },
  computed: {
    showSwiper() {
      return this.list.length
    }
  }
}
</script>

<style lang="stylus" scoped>
.wrapper >>> .swiper-pagination-bullet-active {
  background: #fff;
}

.wrapper {
  width: 100%;
  background: #eee;

  .swiper-img {
    width: 100%;
  }
}
</style>
