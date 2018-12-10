<template>
  <div>
    <div>
      <div class="weekend-title">周末去哪儿</div>
    </div>
    <ul>
      <li class="weekend-item border-bottom" v-for="item of weekendList" :key="item.id">
        <div class="weekend-item-img-wapper">
          <img class="weekend-item-img" :src="item.imgUrl" />
        </div>
        <div class="weekend-item-info">
          <p class="weekend-item-info-title">{{item.title}}</p>
          <p class="weekend-item-info-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
      weekendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1811/f8/29dfa785277839.jpg_r_640x214_7d051523.jpg',
        title: '阳江温泉知多少',
        desc: '这里的天空和大海让人心旷神怡，配上舒缓的优美音乐，泡个暖暖的温泉岂不美哉'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1811/b8/5d599bbdcf8b57.jpg_r_640x214_2ee055e3.jpg',
        title: '浮在海上的绿洲',
        desc: '南国滨海之城，避寒胜地，有暖暖的阳光，海风习习，吃着海鲜逛逛老街多惬意啊'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import "~styles/mixins.styl"
  .weekend-title
    background-color #eee
    padding 0rem .2rem
    line-height .8rem
    font-size: .28rem
  .weekend-item-img-wapper
    height 0
    overflow hidden
    padding-bottom 33.9%
    .weekend-item-img
      width 100%
  .weekend-item-info
    padding .2rem
    min-width 0
    .weekend-item-title
      line-height .54rem
      font-size .28rem
      ellipsis()
    .weekend-item-info-desc
      line-height .4rem
      color #ccc
      font-size .24rem
      padding-top .1rem
      padding-right 1.4rem
      ellipsis()
</style>
