<template>
  <div class="city-search">
    <input class="city-search-input" type="text" placeholder="输入城市名或拼音"/>
  </div>
</template>

<script>
export default {
  name: 'CitySearch'
}
</script>

<style lang="stylus" scoped>
  @import "~styles/varibles.styl"
  .city-search
    height .72rem
    background-color $bgColor
    padding 0 .1rem
    .city-search-input
      line-height .62rem
      height .62rem
      width 100%
      text-align center
      border-radius .06rem
      color #666666
      padding 0 .2rem
      box-sizing border-box
</style>
