<template>
  <div class="city-header">
    <router-link to="/">
    <div class="iconfont city-header-back">&#xe624;</div>
    </router-link>
    城市选择
  </div>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<style lang="stylus" scoped>
  @import "~styles/varibles.styl"
  .city-header
    position relative
    background-color $bgColor
    color #ffffff
    overflow hidden
    height $headerHeight
    line-height $headerHeight
    text-align center
    font-size .32rem
    .city-header-back
      position absolute
      color #ffffff
      width .64rem
      text-align center
      font-size .4rem
      padding-left .2rem
</style>
