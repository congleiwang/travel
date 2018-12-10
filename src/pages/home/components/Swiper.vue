<template>
  <div class="wrapper">
    <swiper :options="swiperOption" v-if="showSwiper">
      <!-- slides -->
      <swiper-slide v-for='item of list' :key="item.id">
        <img class='img-swiper' :src="item.imgUrl" />
      </swiper-slide>
      <!-- Optional controls -->
      <div class="swiper-pagination" slot="pagination"></div>
      <!--<div class="swiper-button-prev" slot="button-prev"></div>-->
      <!--<div class="swiper-button-next" slot="button-next"></div>-->
      <!--<div class="swiper-scrollbar" slot="scrollbar"></div>-->
    </swiper>
  </div>
</template>
<script>
export default {
  name: 'HomeSwiper',
  props: {
    list: Array
  },
  data () {
    return {
      swiperOption: {
        autoplay: {
          stopOnLastSlide: false
        },
        pagination: {
          el: '.swiper-pagination'
        },
        loop: true
      }
    }
  },
  computed: {
    showSwiper () {
      return this.list.length
    }
  }
}
</script>

<style lang="stylus" scoped>
  /*直接穿透入swiper组件*/
  .wrapper >>> .swiper-pagination-bullet-active
    background-color: #ffffff

  .wrapper
    width: 100%
    height: 0
    overflow: hidden
    padding-bottom: 26.66667%
    background-color: #eeeeee

    .img-swiper
      width: 100%
</style>
