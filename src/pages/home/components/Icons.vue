<template>
  <div class="icons">
    <swiper :options="swiperOption"  >
      <swiper-slide v-for="(page,index) of pages" :key="index">
        <div class="icons-icon" v-for="item of page" :key="item.id">
          <div class="icons-icon-img">
            <img class="icons-icon-img-content" :src='item.imgUrl' />
          </div>
          <p class="icons-icon-desc">{{item.desc}}</p>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  props: {
    list: Array
  },
  data () {
    return {
      swiperOption: {
        autoplay: false
      }
    }
  },
  computed: {
    pages () {
      const pages = []
      this.list.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (pages[page] == null) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import "~styles/varibles.styl"
  @import "~styles/mixins.styl"
  .icons
    overflow: hidden
    width: 100%
    height: 0
    padding-bottom: 50%
    background-color #ffffff
    margin-top: .1rem

    .icons-icon
      position: relative
      overflow: hidden
      float: left
      width: 25%
      height: 0
      padding-bottom: 25%

      .icons-icon-img
        position: absolute
        left: 0
        top: 0
        right: 0
        bottom: .40rem
        -webkit-box-sizing: border-box
        -moz-box-sizing: border-box
        box-sizing: border-box

        .icons-icon-img-content
          display: block
          margin: .1rem auto 0 auto
          height: 90%

      .icons-icon-desc
        position: absolute
        left: 0
        right: 0
        bottom: 0
        line-height: .44rem
        height: .44rem
        color: $darkTextColor
        text-align: center
        ellipsis()
</style>
