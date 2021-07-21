<template>
  <div class="swiper">
    <swiper :options="swiperOption">
      <!-- slides -->
      <swiper-slide v-for="item of list" :key="item.id" v-if="list.length">
        <img class="img-box" :src="item.imgUrl" alt="banner">
      </swiper-slide>

    </swiper>
    <!-- Optional controls -->
    <div class="swiper-pagination"></div>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  props: {
    list: Array
  },
  data () {
    return {
      swiperOption: {
        autoplay: 1000,
        loop: true,
        pagination: '.swiper-pagination'
      }
    }
  }
}
</script>

<style lang="stylus" scoped>
.swiper >>> .swiper-pagination-bullet
  margin  0 3px
  background rgb(0 0 255)
.swiper
  height auto
  overflow hidden
  position relative
  .swiper-pagination
     width 100%
     bottom 5px !important
</style>
