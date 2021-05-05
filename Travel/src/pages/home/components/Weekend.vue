<template>
  <div class="weekend">
     <div class="rec-title pg-zy-15">Go To Where In Weeks</div>
     <div class="rec-content fix flex-wrap-wrap mg-zy-15 my-zy-15 pb-zy-15 border-bottom" v-for="item of WeekendList" :key="item.id">
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
  name: "HomeWeekend",
  data () {
      return {
        WeekendList: [{
            id:'001',
            imgUrl: 'https://imgaz.staticbg.com/banggood/os/202104/20210428014629_768.jpg.webp',
            title: 'New Arrival',
            desc: 'udf dfgdg dfsgs iodvncs sdbnsd'
          }, {
            id:'002',
            imgUrl: 'https://imgaz.staticbg.com/banggood/os/202104/20210421215723_318.jpg.webp',
            title: 'Best Sellers',
            desc: 'ghgfh rth hd jisdf ldfmf'
          }, {
            id:'003',
            imgUrl: 'https://imgaz.staticbg.com/banggood/os/202104/20210430045157_761.jpg.webp',
            title: 'Flash Deals',
            desc: ' efsd ferfg jmnsdk dfmmsd ksdm'   
          }, {
            id:'004',
            imgUrl: 'https://imgaz.staticbg.com/banggood/os/202104/20210428014629_768.jpg.webp',
            title: 'Clearance ',
            desc: ' adfr fdggg rtg dfnj jdsk'
          }, {
            id:'005',
            imgUrl: 'https://imgaz.staticbg.com/banggood/os/202104/20210421010332_687.jpg.webp',
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