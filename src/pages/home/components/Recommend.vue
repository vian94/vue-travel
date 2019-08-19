<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li
        class="item border-bottom"
        v-for="item of recommendList"
        :key="item.id">
        <img class="item-img" :src="item.imgUrl">
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
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
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1503/' +
          'b4/b4834f16bc8f8091.water.jpg_200x200_be5f7395.jpg',
        title: '珠海长隆海洋王国',
        desc: '大型鲸鲨展馆，超长飞行过山车'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1503/' +
          'b4/b4834f16bc8f8091.water.jpg_200x200_be5f7395.jpg',
        title: '珠海长隆海洋王国',
        desc: '大型鲸鲨展馆，超长飞行过山车'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1503/' +
          'b4/b4834f16bc8f8091.water.jpg_200x200_be5f7395.jpg',
        title: '珠海长隆海洋王国',
        desc: '大型鲸鲨展馆，超长飞行过山车'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .title
    margin-top .2rem
    line-height .8rem
    background #eee
    text-indent .2rem
  .item
    display flex
    height 1.9rem
    overflow hidden
    .item-img
      width 1.7rem
      height 1.7rem
      padding .1rem
    .item-info
      flex 1
      padding .1rem
      min-width 0
      .item-title
        line-height .54rem
        font-size .32rem
        ellipsis()
      .item-desc
        line-height .4rem
        color #ccc
        ellipsis()
      .item-button
        line-height .44rem
        margin-top .16rem
        background #ff9300
        padding 0 .3rem
        border-radius .06rem
        color #fff
</style>
