<template>
  <div class="container">
    <div class="wrapper">
      <swiper :options="swiperOptions">
        <!-- slides -->
        <swiper-slide>
          <img class="gallary-img"
               src="http://img1.qunarzz.com/sight/p0/1908/60/6014c4a3b92fb074a3.img.jpg_r_800x800_2263c623.jpg"/>
        </swiper-slide>
        <swiper-slide>
          <img class="gallary-img"
               src="http://img1.qunarzz.com/sight/p0/1908/f4/f4842597d1d58d18a3.img.jpg_r_800x800_57e80517.jpg"/>
        </swiper-slide>
        <!-- Optional controls -->
        <div class="swiper-pagination" slot="pagination"></div>
      </swiper>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CommonGallary',
  props: {
    imgs: {
      type: Array,
      default () {
        return []
      }
    }
  },
  data () {
    return {
      swiperOptions: {
        pagination: '.swiper-pagination',
        paginationType: 'fraction',
        loop: true
      }
    }
  }
}
</script>

<style lang="stylus" scoped>
  .container >>> .swiper-container
    overflow inherit
    height 0
    padding-bottom 55%
  .container
    display flex
    flex-direction column
    justify-content center
    z-index 99
    position fixed
    left 0
    right 0
    top 0
    bottom 0
    background #000
    .wrapper
      height 0
      width 100%
      padding-bottom 55%
      .gallary-img
        width 100%
      .swiper-pagination
        color #fff
        bottom -2rem
</style>
