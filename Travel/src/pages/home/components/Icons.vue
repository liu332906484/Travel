<template>
  <div class="icons-box">
    <swiper :options="swiperOption">
      <!-- slides -->
      <swiper-slide class="fix align-items-center flex-wrap-wrap" v-for="(page, index) of pages" :key="index">
        <div class="icons-img fix align-items-center flex-direction my-zy-15" v-for="item of page" :key="item.id">
          <div class="icons-img-contenct">
             <img class="img-box" :src="item.imgUrl" alt="item.desc">
          </div>
          <div class="icons-img-text mt-zy-10">{{item.desc}}</div>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  props: {
    iconlist: Array
  },
  data () {
    return {
      swiperOption: {
        autoplay: false
      }
    }
  },
  computed: {
    pages () {
      const pages = []
      this.iconlist.forEach((item, index) => {
        const page = Math.floor(index/8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>

<style lang="stylus" scoped>
  .icons-box
     box-sizing border-box
     clear both
     height auto
     .icons-img
       width 25%
       .icons-img-contenct
         width 60%
       .icons-img-text
         font-size 0.26rem
         color #999
</style>
