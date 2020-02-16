<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl" alt />
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
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
      },
      swiperList: [
        {
          id: '0001',
          imgUrl:
            'http://img1.qunarzz.com/sight/source/1603/13/eab38d3176c6cc.jpg_r_640x214_acdb891e.jpg'
        },
        {
          id: '0002',
          imgUrl:
            'http://img1.qunarzz.com/sight/source/1510/de/2c2ca6e158f80f.jpg_r_640x214_2385de27.jpg'
        }
      ]
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
