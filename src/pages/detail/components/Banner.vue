<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" :src="this.bannerImg" alt="">
      <div class="banner-info">
        <div class="banner-title">{{this.sightName}}</div>
        <div class="banner-number"><span class="iconfont arrow-icon banner-icon">&#xe63e;</span>{{this.gallaryImgs.length}}</div>
      </div>
    </div>
    <fade-animation>
      <common-gallary
        :imgs="gallaryImgs"
        v-show="showGallary"
        @close="handleGallaryClose"></common-gallary>
    </fade-animation>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
import FadeAnimation from 'common/fade/Fade'
export default {
  name: 'DetailBanner',
  props: {
    sightName: String,
    bannerImg: String,
    gallaryImgs: Array
  },
  data () {
    return {
      showGallary: false
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
    CommonGallary,
    FadeAnimation
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
