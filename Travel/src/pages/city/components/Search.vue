<template>
  <div>
    <div class="search fix align-items-center">
        <div class="search-box c-b-l mg-zy-10">
             <input class="search-input" type="search" name="search" placeholder="请输入城市或拼音" v-model="keyword" />
        </div>
    </div>
    <div class="search-content" v-show="keyword" ref="search">
          <ul class="search-item py-zy-5">
             <li class="search-list py-zy-10 pg-zy-15 border-bottom" v-for="item of list" :key="item.id" @click="handleCityClick(item.name)">{{item.name}}</li>
             <li class="search-list py-zy-10 pg-zy-15 border-bottom" v-show="hasNoDate">没有匹配到你搜索的城市</li>
          </ul>
    </div>
  </div>
</template>

<script>
import BetterScroll from 'better-scroll'
import { mapMutations } from 'vuex'
export default {
  name: 'CitySearch',
  props: {
    cities: Object
  },
  data () {
    return {
      keyword: '',
      list: [],
      timer: null
    }
  },
  watch: {
    keyword () {
      if (this.timer) {
        clearTimeout(this.timer)
      }

      if (!this.list) {
        this.list = []
        return
      }

      this.timer = setTimeout(() => {
        const result = []
        for (let i in this.cities) {
          this.cities[i].forEach((value) => {
            if (value.spell.indexOf(this.keyword) > -1 || value.name.indexOf(this.keyword) > -1 ) {
              result.push(value)
            }
          })
        }
        this.list = result
      }, 100)
    }
  },
  computed: {
    hasNoDate () {
      return !this.list.length
    }
  },
  methods: {
    handleCityClick (city) {
      this.changeCity(city)
      this.$router.push('/')
    },
    ...mapMutations(['changeCity'])
  },
  mounted () {
    this.scroll = new BetterScroll(this.$refs.search)
  }
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
  .search-content
     position absolute
     left 0
     right 0
     bottom 0
     top 1.4rem
     background #eee
     z-index 2
     .search-item
        background #fff
        .search-list
          line-height 0.32rem
          font-size 0.24rem
</style>
