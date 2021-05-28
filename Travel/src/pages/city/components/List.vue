<template>
    <div class="list" ref="warpper">
         <div>
            <div class="area">
                <div class="title fix align-items-center"><div class="mg-zy-20">你的定位</div></div>
                <div class="area-box fix align-items-center flex-wrap-wrap mg-zy-10 my-zy-10">
                    <div class="area-wrap"> <div class="area-item" v-for="item of Cityposition" :key="item.id">{{item.name}}</div> </div>
                </div>
            </div>
            <div class="area">
                <div class="title fix align-items-center"><div class="mg-zy-20">去过的地方</div></div>
                <div class="area-box fix align-items-center flex-wrap-wrap mg-zy-10 my-zy-10">
                    <div class="area-wrap" v-for="item of hotCities" :key="item.id">
                         <div class="area-item">{{item.name}}</div> 
                    </div>
                </div>
            </div>
            <div class="area" v-for ="(item, key) of cities" :key="key" :ref="key">
                <div class="title fix align-items-center"><div class="mg-zy-20">{{key}}</div></div>
                <div class="area-content fix align-items-center flex-wrap-wrap mg-zy-20 my-zy-15">
                    <div class="area-wrap-list border-bottom" v-for = 'innerHTML of item' :key="innerHTML.id"> <div class="area-item my-zy-15">{{innerHTML.name}}</div> </div>
                </div>
            </div>
         </div>
    </div>
</template>

<script>
import BetterScroll from 'better-scroll'
export default {
    name:'CityList',
    props: {
         Cityposition: Array,
         cities: Object,
         hotCities: Array,
         letter: String
    },
    mounted() {
        this.scroll = new BetterScroll(this.$refs.warpper, {movable: true, zoom: true, pullUpLoad: true})
    },
    watch: {
        letter () {
           if (this.letter) {
              const el = this.$refs[this.letter][0]
              this.scroll.scrollToElement(el)
           }
        }
    }
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl'
.list
  position absolute
  overflow hidden
  top 1.4rem
  bottom 0
  left 0 
  right 0
  background #fff
  .area
    .title
      height $bgheight6
      background $bggrayd
      font-size .28rem
    .area-box
      .area-wrap
        width 23%
        height $bgheight5
        font-size .24rem
        margin 1%
        .area-item
          box-sizing border-box
          border 1px $bggrayd solid 
          text-align center 
          line-height $bgheight5
          border-radius .06rem
    .area-content
      width 100%
      .area-wrap-list
         width 100%
         height $bgheight5
         font-size .24rem
</style>