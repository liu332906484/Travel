<template>
  <div class="recommend">
     <div class="rec-title pg-zy-15">Hots Recommend</div>
     <div class="rec-content fix flex-wrap-wrap mg-zy-15 my-zy-15 pb-zy-15 border-bottom" v-for="item of recommendList" :key="item.id">
         <div class="rec-img mr-zy-15">
             <img class="img-box" :src="item.imgUrl" alt="item.desc">
         </div>
         <div class="rec-text-content flx-flex">
             <div class="rec-title-text mt-zy-15">{{item.title}}</div>
             <div class="rec-desc mt-zy-15">{{item.desc}}</div>
             <button class="rec-bottom mt-zy-15">Check the details</button>
         </div>
     </div>
  </div>
</template> 

<script>
export default {
  name: "HomeRecommend",
  data () {
      return {
        recommendList: [{
            id:'001',
            imgUrl: 'https://imgaz1.chiccdn.com/thumb/grid/oaupload/newchic/images/A6/59/73ba3adc-4ffe-4b71-833a-c86f8ba73145.jpg.webp?s=163x217',
            title: 'New Arrival',
            desc: 'udf dfgdg dfsgs iodvncs sdbnsd'
          }, {
            id:'002',
            imgUrl: 'https://imgaz1.chiccdn.com/thumb/grid/oaupload/newchic/images/02/AF/7d10e0b8-b685-4b25-95b4-afcae14f1178.jpg.webp?s=163x217',
            title: 'Best Sellers',
            desc: 'ghgfh rth hd jisdf ldfmf'
          }, {
            id:'003',
            imgUrl: 'https://imgaz1.chiccdn.com/thumb/grid/oaupload/newchic/images/DF/87/c818aec7-9759-4c37-b083-2dc479f87f2c.jpg.webp?s=163x217',
            title: 'Flash Deals',
            desc: ' efsd ferfg jmnsdk dfmmsd ksdm'   
          }, {
            id:'004',
            imgUrl: 'https://imgaz1.chiccdn.com/thumb/grid/oaupload/newchic/images/86/42/d12aa601-db6f-42cd-82d4-6bfa3b8879bf.jpg.webp?s=163x217',
            title: 'Clearance ',
            desc: ' adfr fdggg rtg dfnj jdsk'
          }, {
            id:'005',
            imgUrl: 'https://imgaz1.chiccdn.com/thumb/grid/oaupload/newchic/images/A6/59/73ba3adc-4ffe-4b71-833a-c86f8ba73145.jpg.webp?s=163x217',
            title: 'Patchwork ',
            desc: ' fsf fgwe fasdf opjfskd'  
          }
        ]
      }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .rec-title
    line-height $bgheight6
    font-size 0.32rem
    background $bgColor
    color #fff
  .rec-content 
    .rec-img
        width $bgheight20
  .rec-text-content  
    .rec-title-text
      color $bggray
      font-size 0.30rem
    .rec-desc
      color $bggray1
      font-size 0.24rem
    .rec-bottom
      color #fff
      padding 0.1rem 0.2rem
      font-size 0.24rem
      background $bgColor
      border-radius .05rem
</style>