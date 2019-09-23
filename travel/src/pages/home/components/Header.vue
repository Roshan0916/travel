<template>
  <div class="header">
    <div class="header-left">
        <img :src="url" class="icon">
        返回</div>
    <div class="header-input">
        <img :src="url1" class="icon">
        输入城市/景点/游玩主题</div>
        <router-link to='/city'>
          <div class="header-right">{{this.city}}
              <img :src="url2" class="icon">
          </div>
        </router-link>
  </div>
</template>
<script>
import { mapstate, mapState} from 'vuex'
export default {
  name: 'HomeHeader',
  computed:{
    ...mapState(['city'])
  },
  props: {
    city: String
  },
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
    display: flex
    line-height: .86rem
    background: $bgColor
    color: #fff
    .header-left
      width: .8rem
      float: left
      .icon
        height: .25rem
    .header-input
      padding-left: .2rem
      height: .64rem
      line-height: .64rem
      flex: 1
      border-radius: .1rem
      margin: .12rem 0 0 .2rem
      background: #fff
      color:#ccc
      .icon
        height: .4rem
    .header-right
      margin-left: .1rem
      min-width: 1.04rem
      float: right
      color:#fff
      .icon
        height: .25rem
</style>
