<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" src="//img1.qunarzz.com/sight/p0/1505/bf/bfe6ec0e88e5c68a.water.jpg_600x330_b6374200.jpg" alt="">
      <div class="banner-info">
        <div class="banner-title">大连涉亚海洋世界</div>
        <div class="banner-number"><span class="iconfont arrow-icon banner-icon">&#xe63e;</span>39</div>
      </div>
    </div>
    <common-gallary
      :imgs="imgs"
      v-show="showGallary"
      @close="handleGallaryClose"></common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'DetailBanner',
  data () {
    return {
      showGallary: false,
      imgs: ['http://img1.qunarzz.com/sight/p0/201309/06/31fc67f037f2b079c8d65eac.jpg_r_800x800_ebdd868a.jpg']
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleGallaryClose () {
      this.showGallary = false
    }
  },
  components: {
    CommonGallary
  }
}
</script>

<style lang="stylus" scoped>
  .banner
    position: relative
    overflow :hidden
    height:0
    padding-bottom :55%
    .banner-img
      width: 100%
    .banner-info
      display: flex
      position: absolute
      left:0
      right:0
      bottom:0
      color: #fff
      line-height:.6rem
      background-image :linear-gradient(top ,rgba(0,0,0,0),rgba(0,0,0,0.8))
      .banner-title
        font-size :.32rem
        padding: 0 .2rem
        flex:1
      .banner-number
        line-height: .32rem
        height: .32rem
        margin-top :.14rem
        padding:0 .4rem
        font-size: .24rem
        border-radius: .2rem
        background :rgba(0,0,0, .8)
        .banner-icon
          padding-right :.06rem
          font-size :.24rem
</style>
