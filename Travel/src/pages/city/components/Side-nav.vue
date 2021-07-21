<template>
   <div class="side-nav">
      <ul class="side-list">
        <li class="side-item" v-for="item of letters" @click="handLetterClick" @touchstart="handTouchStart" @touchmove="handTouchMove" @touchend="handTouchEnd" :ref="item">{{item}}</li>
      </ul>
   </div>
</template>

<script>
export default {
    name: 'Side-Nav',
    props: {
         cities: Object,
    },
    data() {
      return {
        TouchStacts: false,
        startY: 0,
        timer: null,
      }
    },
    updated() {
      this.startY = this.$refs['A'][0].offsetTop
    },
    computed: {
      letters () {
        const letters = []
        for (let i in this.cities) {
           letters.push(i)
        }
        return letters
      }  
    },
    methods: {
      handLetterClick (e) {
         //console.log(e.target.innerText)
         this.$emit('change', e.target.innerText)
      },
      handTouchStart () {
         this.TouchStacts = true
      },
      handTouchMove (e) {
         if (this.TouchStacts) {
           if (this.timer) {
               clearTimeout(this.timer)
           }
           this.timer = setTimeout ( () => {
            const touchY =  e.touches[0].clientY 
            const index = Math.floor( (touchY - this.startY ) / 19 ) 
            if (index >= 0 && index < this.letters.length ) {
                this.$emit('change', this.letters[index])
            }
           }, 16)

         }
      },
      handTouchEnd () {
        this.TouchStacts = false
      }
    },
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .side-nav
    position absolute
    top  0
    bottom 0
    right 0
    width .38rem
    .side-list
      display flex
      justify-content  center
      align-items center
      flex-direction column
      height 100%
      .side-item
        line-height 0.38rem
        text-align center
        color #333
        background #fff
        width 100%
</style>