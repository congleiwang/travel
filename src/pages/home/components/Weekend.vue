<template>
  <div>
    <div>
      <div class="weekend-title">周末去哪儿</div>
    </div>
    <ul>
      <li class="weekend-item border-bottom" v-for="item of list" :key="item.id">
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
  props: {
    list: Array
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
    padding-bottom 36.64%
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
