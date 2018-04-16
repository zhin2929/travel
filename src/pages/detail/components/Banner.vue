<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" src="http://img1.qunarzz.com/sight/p0/1803/7b/7b023b9728f0834fa3.img.jpg_600x330_5f4c76f7.jpg" />
      <div class="banner-info">
        <div class="banner-tittle">
          AAAAAAAAAAAAAAAAAA
        </div>
        <div class="banner-number">
          <span class="iconfont banner-icon">&#xe692;</span>
          33
        </div>
      </div>
    </div>
    <common-gallary @close="handleGallaryClose" :imgs="imgs" v-show="showGallary"></common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'DetailBanner',
  data () {
    return {
      showGallary: false,
      imgs: [
        'http://img1.qunarzz.com/sight/p0/1803/19/19ab540e316d22ba3.img.jpg_350x240_d3438e1a.jpg',
        'http://img1.qunarzz.com/sight/p0/1803/19/19ab540e316d22ba3.img.jpg_350x240_d3438e1a.jpg'
      ]
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
    overflow: hidden
    height: 0
    padding-bottom: 55%
    .banner-img
      width: 100%
    .banner-info
      display: flex
      position: absolute
      left: 0
      right: 0
      bottom: 0
      line-height: .6rem
      color: #fff
      background-image: linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.8))
      .banner-tittle
        flex: 1
        font-size: .32rem
        padding: 0 .2rem
      .banner-number
        height: .32rem
        line-height: .32rem
        margin-top: .14rem
        padding: 0 .4rem
        border-radius: .2rem
        background: rgba(0, 0, 0, .8)
        font-size: .24rem
        .banner-icon
          font-size: .24rem
</style>
