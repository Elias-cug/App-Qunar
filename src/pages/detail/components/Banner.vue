<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" src="//img1.qunarzz.com/sight/p0/1712/95/95f38f28a6ff19cba3.img.jpg_600x330_682f736a.jpg" />
      <div class="banner-info">
        <div class="banner-title">水奥雪世界</div>
        <div class="banner-number">
          <span class="iconfont banner-icon">&#xe648;</span>
          39
        </div>
      </div>
    </div>
    <common-gallary :imgList="imgList" v-show="showGallary" @close="handleGalleryClose"></common-gallary>
  </div>
</template>
<script>
import CommonGallary from 'common/gallary/gallary.vue'
export default {
  name: 'DetailBanner',
  components: {
    CommonGallary
  },
  data () {
    return {
      showGallary: false,
      imgList: ['http://img1.qunarzz.com/sight/p0/1812/36/3681190a5aeb0d79a3.img.jpg_350x240_591bd36b.jpg',
        'http://img1.qunarzz.com/sight/p0/1712/95/95f38f28a6ff19cba3.img.jpg_350x240_2fa80d8d.jpg']
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleGalleryClose () {
      this.showGallary = false
    }
  }
}
</script>
<style lang="stylus" scoped>
  .banner
    position relative
    overflow hidden
    height 0
    padding-bottom 55%
    .banner-img
      width 100%
    .banner-info
      display flex
      position absolute
      right 0
      bottom 0
      left 0
      line-height .6rem
      color #fff
      background-image linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.8))
      .banner-title
        flex 1
        font-size .32rem
        padding 0 .2rem
      .banner-number
        height .4rem
        line-height .4rem
        padding 0 .4rem
        margin-top .14rem
        border-radius .2rem
        background rgba(0, 0, 0, .8)
        font-size .24rem
        .banner-icon
          font-size .24rem
</style>
