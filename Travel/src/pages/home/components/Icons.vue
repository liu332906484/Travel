<template>
  <div class="icons-box">
    <swiper>
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
  data () {
    return {
      iconsList: [{
        id: '001',
        imgUrl: 'https://imgaz1.chiccdn.com/os/202104/20210425215012_911.png.webp',
        desc: 'Tops'
      }, {
        id: '002',
        imgUrl: 'https://imgaz1.chiccdn.com/os/202104/20210425215353_754.png.webp',
        desc: 'Bottoms'
      }, {
        id: '003',
        imgUrl: 'https://imgaz1.chiccdn.com/os/202104/20210425215421_302.png.webp',
        desc: 'Dresses'
      }, {
        id: '004',
        imgUrl: 'https://imgaz1.chiccdn.com/os/202104/20210425215446_199.png.webp',
        desc: 'Lingerie'
      }, {
        id: '005',
        imgUrl: 'https://imgaz1.chiccdn.com/os/202104/20210425215742_733.png.webp',
        desc: 'Shoes'
      }, {
        id: '006',
        imgUrl: 'https://imgaz1.chiccdn.com/os/202104/20210425215809_345.png.webp',
        desc: 'Bags'
      }, {
        id: '007',
        imgUrl: 'https://imgaz1.chiccdn.com/os/202104/20210425215834_464.png.webp',
        desc: 'Acc & Beauty'
      }, {
        id: '008',
        imgUrl: 'https://imgaz1.chiccdn.com/os/202104/20210425215858_943.png.webp',
        desc: 'Home'
      }, {
        id: '009',
        imgUrl: 'https://imgaz1.chiccdn.com/os/202104/20210425225658_421.png.webp',
        desc: 'Patchwork'
      }, {
        id: '010',
        imgUrl: 'https://imgaz1.chiccdn.com/os/202104/20210425230009_787.png.webp',
        desc: 'Flower'
      }]
    }
  },
  computed: {
    pages () {
      const pages = []
      this.iconsList.forEach((item, index) => {
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
