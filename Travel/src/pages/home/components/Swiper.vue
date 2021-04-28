<template>
  <div class="swiper">
    <div v-swiper:mySwiper="swiperOption">
      <div class="swiper-wrapper">
        <div class="swiper-slide" v-for="banner in banners">
          <img class="img-box" :src="banner">
        </div>
      </div>
      <div class="swiper-pagination"></div>
    </div>
  </div>
</template> 

<script>
export default {
  name: "HomeSwiper",
  data () {
    return {
      banners: ['https://imgaz.staticbg.com/banggood/os/202104/20210427045140_735.jpg.webp', 'https://imgaz.staticbg.com/banggood/os/202104/20210427045140_735.jpg.webp'],
      swiperOption: {
        pagination: {
          el: '.swiper-pagination'
        }
      }
    }
  }
};
</script>

<style lang="stylus" scoped>
  .swiper
    width 100%
    .swiper-slide
      width 100%
</style>