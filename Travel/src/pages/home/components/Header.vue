<template>
  <div class="header">
    <div class="header-item h-l"><span class="iconarrow-down-bold"></span></div>
    <div class="header-item h-c">搜索</div>
    <div class="header-item h-r">城市</div>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader'
}
</script>

<style lang='stylus' scoped>
  .header
    height .86rem
    display flex
    background #0bc4d0
    align-items center
    justify-items center
    justify-content space-between
    font-size .26rem
    color #fff
    text-align center
    .h-l
      width .64rem
      font-size .32rem
    .h-c
      flex 1
      background #fff
      height .6rem
      line-height .6rem
      border-radius .05rem
      color #aaa
      padding 0 0.2rem
      text-align left
    .h-r
      width 1.20rem
</style>
