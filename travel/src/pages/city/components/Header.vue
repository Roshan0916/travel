<template>
  <div class="header">
    <router-link to="/">
      <img :src="url" class="header-back">
    </router-link>
    城市选择
  </div>
</template>
<script>
export default {
  name: 'CityHeader',
  data () {
    return {
      url: '/../../../static/images/fanhui.png',
      url1: '/../../../static/images/fangdajing.png',
      url2: '/../../../static/images/xiala.png'
    }
  }
}
</script>
<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .header
    position :relative
    overflow: hidden
    height 0.86rem
    line-height:.86rem
    text-align:center
    color:#fff
    background :$bgColor
    font-size: .32rem
    .header-back
      position:absolute
      left:0
</style>