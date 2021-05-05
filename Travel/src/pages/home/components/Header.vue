<template>
  <div class="header fix align-items-center justify-content-between ">
     <div class="header-box h-b-l mg-zy-10">
       <div class="fix align-items-center justify-content-center">
          <i class="iconfont iconarrow-left-bold"></i>
       </div>
     </div>
     <div class="header-box h-b-c flx-flex">
       <div class="fix align-items-center justify-content-center">
          <span class="search pg-zy-15"><i class="iconfont iconsearch"></i> makeing ing...... </span>
       </div>
     </div>
     <div class="header-box h-b-r mg-zy-10">
       <div class="fix align-items-center justify-content-center">
          <span class="city">City</span><i class="iconfont iconmap mg-yz-5"></i>
       </div>
     </div>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader'
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .header
    height $bgheight8
    background $bgColor
    color #fff
    font-size 0.32rem
    .header-box
      .search
        width 100%
        height $bgheight5
        line-height $bgheight5
        background #fff
        color #999
        font-size 0.24rem
        border-radius 0.05rem
        .iconsearch
          font-size 0.28rem
      .city
        font-size 0.28rem
    .h-b-l
      width $bgheight5
    .h-b-r
      width $bgheight12
</style>
