<template>
  <div class='header'>
    <div class='header-left'>
      <div class="iconfont icon-back">&#xe624;</div>
    </div>
    <div class='header-input'>
      <span class="iconfont">&#xe632;</span>
      输入城市/景点/游玩主题
    </div>
    <router-link to="/city">
      <div class='header-right' >{{this.city}}<span class="iconfont icon-arrow-down">&#xe64a;</span></div>
    </router-link>

  </div>
</template>

<script>
export default {
  name: 'HomeHeader',
  props: {
    city: String
  }
}
</script>

<style lang="stylus" scoped>
  @import "~styles/varibles.styl"
  .header
    display: flex
    line-height: $headerHeight
    background-color: $bgColor
    color: #ffffff

    .header-left
      width: .64rem
      float: left
      .icon-back
        text-align: center
        font-size: .4rem

    .header-input
      flex: 1
      text-indent: .2rem
      height: .64rem
      line-height: .64rem
      margin-top: .12rem
      margin-left: .2rem
      background-color: #ffffff
      border-radius: .1rem
      color: #cccccc

    .header-right
      width: 1.24rem
      float: right
      text-align: center
      color: #ffffff
      .icon-arrow-down
        font-size: .3rem
        margin-left .02rem
</style>
