<template>
  <div class="swiper">
    <swiper :options="swiperOption">
      <!-- slides -->
      <swiper-slide>
        <img class="img-box" src="https://imgaz.staticbg.com/banggood/os/202104/20210427045140_735.jpg.webp" alt="banner">
      </swiper-slide>
      <swiper-slide>
        <img class="img-box" src="https://imgaz.staticbg.com/banggood/os/202104/20210422215132_171.jpg.webp" alt="banner">
      </swiper-slide>
      <swiper-slide>
        <img class="img-box" src="https://imgaz.staticbg.com/banggood/os/202104/20210421215723_318.jpg.webp" alt="banner">
      </swiper-slide>
      <swiper-slide>
        <img class="img-box" src="https://imgaz.staticbg.com/banggood/os/202104/20210429035146_531.jpg.webp" alt="banner">
      </swiper-slide>
      <!-- Optional controls -->
      <div class="swiper-pagination"></div>
    </swiper>
  </div>
</template> 

<script>
export default {
  name: "HomeSwiper",
  data () {
    return {
      swiperOption: {
          autoplay: 1000,
          loop: true,
          pagination: {
            el: '.swiper-pagination',
            clickable: true
          }
      }
    }
  }
}
</script>

<style lang="stylus" scoped>
.swiper
  height auto 
  overflow hidden
  .swiper-container
     width 100%
</style>