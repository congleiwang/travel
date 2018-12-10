<template>
  <div>
    <div class="recommend-title">
      <img class="recommend-title-like" src="http://img1.qunarzz.com/piao/fusion/1711/89/ebc329f16c55bb02.png" />
      <span>猜你喜欢</span>
    </div>
    <ul>
      <li class="recommend-item border-bottom" v-for="item of recommendList" :key="item.id">
        <img class="recommend-item-img" :src="item.imgUrl" />
        <div class="recommend-item-info">
          <p class="recommend-item-info-title">{{item.title}}</p>
          <p class="recommend-item-info-desc">{{item.desc}}</p>
          <button class="recommend-item-info-btn">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1502/15/15ca1d0eab6bf46c.water.jpg_200x200_50ca7bb1.jpg',
        title: '东部华侨城大侠谷',
        desc: '行走峡湾栈道，倾听大自然的天籁之音'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1502/15/15ca1d0eab6bf46c.water.jpg_200x200_50ca7bb1.jpg',
        title: '东部华侨城大侠谷',
        desc: '行走峡湾栈道，倾听大自然的天籁之音'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1502/15/15ca1d0eab6bf46c.water.jpg_200x200_50ca7bb1.jpg',
        title: '东部华侨城大侠谷',
        desc: '行走峡湾栈道，倾听大自然的天籁之音'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import "~styles/mixins.styl"
  .recommend-title
    padding .1rem .2rem
    line-height .8rem
    .recommend-title-like
      line-height .3rem
      height .3rem
  .recommend-item
    display flex
    height 1.9rem
    overflow hidden
    .recommend-item-img
      width 1.8rem
      height 1.8rem
      padding .2rem
    .recommend-item-info
      flex 1
      padding .2rem
      min-width 0
      .recommend-item-title
        line-height .54rem
        font-size .32rem
        ellipsis()
      .recommend-item-info-desc
        line-height .4rem
        color #ccc
        padding-top .1rem
        ellipsis()
      .recommend-item-info-btn
        line-height .44rem
        margin-top .2rem
        background-color #ff9300
        padding 0 .2rem
        border-radius .06rem
        color #ffffff
</style>
