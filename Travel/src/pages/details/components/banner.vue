<template>
  <div class="banner">
    <div class="banner-container">
      <img class="img-box" src="@/assets/img/uin-2.jpg" alt="">
      <div class="banner-info">
        <div class="banner-title">
          <span class="banner-span pl-zy-15">mroe in info key</span>
        </div>
        <div class="banner-number">
          <i class="iconfont iconsetting pr-zy-5"></i>32
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DetailsBanner'
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .banner
    .banner-container
      position relative
      height 0
      padding-bottom 41.7%
      overflow hidden
    .banner-info
      position absolute
      bottom 0
      left 0
      right 0
      background linear-gradient(top, rgba(0,0,0,.3), rgba(0,0,0,.05))
      color #FFF
      display flex
      line-height 0.5rem
      .banner-title
         flex 1
         font-size 0.18rem
      .banner-number
        padding 0 0.1rem
        background rgba(255,255,255,0.5)
        min-width 1rem
        height 0.38rem
        margin 0.06rem auto
        color #fff
        text-align center
        line-height 0.38rem
        border-radius 0.5rem 0 0 0.5rem
        .iconsetting
          font-size 0.18rem
</style>
