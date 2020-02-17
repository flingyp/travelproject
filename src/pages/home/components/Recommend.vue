<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <img :src="item.imgUrl" alt class="item-img" />
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data() {
    return {
      recommendList: [
        {
          id: '0001',
          imgUrl:
            'http://img1.qunarzz.com/sight/p0/1807/6d/6d9e3718adecf42a3.img.jpg_250x250_e46bd861.jpg',
          title: '普罗旺斯新风尚农场',
          desc: '玉山普罗旺斯农场门票+项目通票一票畅玩'
        },
        {
          id: '0002',
          imgUrl:
            'http://img1.qunarzz.com/sight/p0/1807/6d/6d9e3718adecf42a3.img.jpg_250x250_e46bd861.jpg',
          title: '普罗旺斯新风尚农场',
          desc: '玉山普罗旺斯农场门票+项目通票一票畅玩'
        },
        {
          id: '0003',
          imgUrl:
            'http://img1.qunarzz.com/sight/p0/1807/6d/6d9e3718adecf42a3.img.jpg_250x250_e46bd861.jpg',
          title: '普罗旺斯新风尚农场',
          desc: '玉山普罗旺斯农场门票+项目通票一票畅玩'
        },
        {
          id: '0004',
          imgUrl:
            'http://img1.qunarzz.com/sight/p0/1807/6d/6d9e3718adecf42a3.img.jpg_250x250_e46bd861.jpg',
          title: '普罗旺斯新风尚农场',
          desc: '玉山普罗旺斯农场门票+项目通票一票畅玩'
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

.item {
  overflow: hidden;
  display: flex;
  height: 1.9rem;

  .item-img {
    width: 1.7rem;
    height: 1.7rem;
    padding: 0.1rem;
  }

  .item-info {
    flex: 1;
    padding: 0.1rem;
    min-width: 0;

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

    .item-button {
      line-height: 0.44rem;
      margin-top: 0.16rem;
      background: #ff9300;
      padding: 0 0.2rem;
      border-radius: 0.06rem;
      color: #fff;
    }
  }
}
</style>
