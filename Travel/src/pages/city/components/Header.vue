<template>
    <div class="city fix align-items-center">
        <div class="city-box c-b-l mg-zy-10">
            <router-link to='/'>
                <div class="city-content fix align-items-center justify-content-center">
                    <i class="iconfont iconarrow-left-bold"></i>
                </div>
            </router-link>
        </div>
        <div class="city-box c-b-r mg-zy-10 flx-flex">
            <div class="city-content fix align-items-center justify-content-center">
                 <div class="city-item city-int mr-zy-10">国内城市</div>
                 <div class="city-item city-out">国外城市</div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'CityHeader'
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .city
    height $bgheight8
    background $bgColor
    color #fff
    font-size 0.32rem
    .c-b-l
      width 0.6rem
      position relative
      z-index 10
      .city-content
        .iconarrow-left-bold
          color $bgwhite
    .c-b-r
      .city-content
        margin-left -0.8rem
        .city-item
          background $bgwhite
          height $bgheight4
          padding 0.05rem 0.3rem
          color $bgColor
          line-height .4rem
          font-size .28rem
          border-radius .05rem
          text-align center
</style>
