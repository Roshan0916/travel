<template>
  <div>
    <router-link
    tag="div"
    to="/"
    class="header-abs"
    v-show="showAbs">
       <img :src="url" class="icon">
    </router-link>
  <div
  class="header-fixed"
  v-show="!showAbs"
  :style="opacityStyle">
    <router-link tag="div" to="/" >
       <img :src="url" class="icon">
    </router-link>
    景点详情
    </div>
  </div>
</template>
<script>
export default {
  name:'DetailHeader',
  data () {
    return {
      showAbs: true,
      opacityStyle : {
        opacity: 0
      },
      url: '/../../../static/images/fanhui.png',
      url1: '/../../../static/images/fangdajing.png',
      url2: '/../../../static/images/xiala.png'
    }
  },
  methods:{
    handleScroll () {
      const top = document.documentElement.scrollTop
      if (top > 60) {
        let opacity = top / 140
        opacity = opacity > 1 ? 1 : opacity
        this.opacityStyle = { opacity }
        this.showAbs = false
      } else {
        this.showAbs = true
      }
    }
  },
  activated () {
    window.addEventListener('scroll', this.handleScroll)
  },
  deactivated () {
    window.removeEventListener('scroll', this.handleScroll)
  }
}
</script>
<style lang="stylus" scoped>
@import '~styles/varibles.styl'
  .header-abs
    position:absolute
    left:.2rem
    top:.2rem
    width:.8rem
    height: .8rem
    border-radius: .4rem
    background: rgba(0,0,0,.8)
    .icon
      height: .5rem
      margin:.2rem 0 0 .2rem
  .header-fixed
    z-index: 2
    position :fixed
    top:0
    left:0
    right:0
    height 0.86rem
    line-height:.86rem
    text-align:center
    color:#fff
    background :$bgColor
    font-size: .32rem
    .icon
      position: absolute
      left:0
      height: .5rem
      margin:.2rem 0 0 .2rem
</style>