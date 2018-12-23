<template>
  <div class="city-list" ref="cityList">
    <div>
      <div class="city-list-area">
        <div class="city-list-area-title border-topbottom">当前城市</div>
        <div class="city-list-area-buttons">
          <div class="city-list-area-buttons-btn-wrapper">
            <div class="city-list-area-buttons-btn">深圳</div>
          </div>
        </div>
      </div>
      <div class="city-list-area border-topbottom">
        <div class="city-list-area-title border-topbottom">热门城市</div>
        <div class="city-list-area-buttons">
          <div class="city-list-area-buttons-btn-wrapper">
            <div class="city-list-area-buttons-btn">深圳</div>
          </div>
          <div class="city-list-area-buttons-btn-wrapper">
            <div class="city-list-area-buttons-btn">深圳</div>
          </div>
          <div class="city-list-area-buttons-btn-wrapper">
            <div class="city-list-area-buttons-btn">深圳</div>
          </div>
          <div class="city-list-area-buttons-btn-wrapper">
            <div class="city-list-area-buttons-btn">深圳</div>
          </div>
          <div class="city-list-area-buttons-btn-wrapper">
            <div class="city-list-area-buttons-btn">深圳</div>
          </div>
          <div class="city-list-area-buttons-btn-wrapper">
            <div class="city-list-area-buttons-btn">深圳</div>
          </div>
          <div class="city-list-area-buttons-btn-wrapper">
            <div class="city-list-area-buttons-btn">深圳</div>
          </div>
        </div>
      </div>
      <div class="city-list-area border-topbottom">
        <div class="city-list-area-title">A</div>
        <div class="city-list-area-items">
          <div class="city-list-area-items-item border-bottom">阿拉善</div>
          <div class="city-list-area-items-item border-bottom">阿拉善</div>
          <div class="city-list-area-items-item border-bottom">阿拉善</div>
          <div class="city-list-area-items-item border-bottom">阿拉善</div>
          <div class="city-list-area-items-item border-bottom">阿拉善</div>
          <div class="city-list-area-items-item border-bottom">阿拉善</div>
          <div class="city-list-area-items-item border-bottom">阿拉善</div>
          <div class="city-list-area-items-item border-bottom">阿拉善</div>
          <div class="city-list-area-items-item border-bottom">阿拉善</div>
          <div class="city-list-area-items-item border-bottom">阿拉善</div>
          <div class="city-list-area-items-item border-bottom">阿拉善</div>
          <div class="city-list-area-items-item border-bottom">阿拉善</div>
          <div class="city-list-area-items-item border-bottom">阿拉善</div>
          <div class="city-list-area-items-item border-bottom">阿拉善</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Bscroll from 'better-scroll'
export default {
  name: 'CityList',
  mounted () {
    this.scroll = new Bscroll(this.$refs.cityList)
  }
}
</script>
<style lang="stylus" scoped>
  .city-list
    position absolute
    top 1.6rem
    left 0
    right 0
    bottom 0
    overflow hidden

  .city-list-area-title
    line-height .44rem
    background-color #eeeeee
    padding-left .2rem
    color #666666
    font-size .26rem

  .city-list-area-buttons
    overflow hidden
    padding .1rem .6rem .1rem .1rem

    .city-list-area-buttons-btn-wrapper
      width 33.33%
      float left

      .city-list-area-buttons-btn
        margin .1rem
        padding .1rem 0
        text-align center
        border .02rem solid #cccccc
        border-radius .06rem

  .city-list-area-items
    .city-list-area-items-item
      line-height .76rem
      padding-left .2rem
</style>
