<template>
  <div class="weekend">
     <div class="rec-title pg-zy-15">Go To Where In Weeks</div>
     <div class="rec-content fix flex-wrap-wrap mg-zy-15 my-zy-15 pb-zy-15 border-bottom" v-for="item of weeklist" :key="item.id">
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
  props: {
    weeklist: Array
  },
  data () {
      return {
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