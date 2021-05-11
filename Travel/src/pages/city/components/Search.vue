<template>
    <div class="search fix align-items-center">
        <div class="search-box c-b-l mg-zy-10">
             <input class="search-input" type="search" name="search" placeholder="请输入城市或拼音" />
        </div>
    </div>
</template>

<script>
export default {
    name: 'CitySearch'
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .search
    height $bgheight6
    background $bgColor
    color $bgwhite
    font-size 0.32rem
    .search-box
      width 100%
      box-sizing border-box
      .search-input
        width 100%
        height $bgheight4
        padding .2rem
        background $bgwhite
        font-size 0.24rem
        color $bggray9
        text-align center
</style>