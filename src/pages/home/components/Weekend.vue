<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <div class="item-img-wrapper">
          <img :src="item.imgUrl" alt class="item-img" />
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data() {
    return {
      recommendList: [
        {
          id: '0001',
          imgUrl:
            'http://img1.qunarzz.com/sight/source/1505/74/a665dfecf12ae.jpg_r_640x214_5d22909a.jpg',
          title: '南昌必游TOP10',
          desc: '看山看水，看看历史对南昌的浸润'
        },
        {
          id: '0002',
          imgUrl:
            'http://img1.qunarzz.com/sight/source/1505/74/a665dfecf12ae.jpg_r_640x214_5d22909a.jpg',
          title: '南昌必游TOP10',
          desc: '看山看水，看看历史对南昌的浸润'
        },
        {
          id: '0003',
          imgUrl:
            'http://img1.qunarzz.com/sight/source/1505/74/a665dfecf12ae.jpg_r_640x214_5d22909a.jpg',
          title: '南昌必游TOP10',
          desc: '看山看水，看看历史对南昌的浸润'
        },
        {
          id: '0004',
          imgUrl:
            'http://img1.qunarzz.com/sight/source/1505/74/a665dfecf12ae.jpg_r_640x214_5d22909a.jpg',
          title: '南昌必游TOP10',
          desc: '看山看水，看看历史对南昌的浸润'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/minis.styl';

.title {
  margin-top: 0.1rem;
  line-height: 0.8rem;
  background: #eee;
  text-align: 0.2rem;
}

.item-img-wrapper {
  overflow: hidden;
  height: 0;
  padding-bottom: 33.9%;
}

.item-img {
  width: 100%;
}

.item-info {
  padding: 0.1rem;

  .item-title {
    line-height: 0.54rem;
    font-size: 0.32rem;
    ellipsis();
  }

  .item-desc {
    line-height: 0.4rem;
    color: #ccc;
    ellipsis();
  }
}
</style>
