<template>
  <div class="list" ref="wrapper">
    <div>
      <div class="area">
        <div class="title">当前城市</div>
        <div class="button-list">
          <div class="button-wrapper">
            <div class="button">北京</div>
          </div>
        </div>
      </div>
      <div class="area">
        <div class="title">热门城市</div>
        <div class="button-list">
          <div class="button-wrapper">
            <div class="button">北京</div>
          </div>
        </div>
      </div>
      <div class="area">
        <div class="title">A</div>
        <div class="item-list">
          <div class="item">
            阿拉尔
          </div>
          <div class="item">
            阿拉尔
          </div>
          <div class="item">
            阿拉尔
          </div>
          <div class="item">
            阿拉尔
          </div>
          <div class="item">
            阿拉尔
          </div>
          <div class="item">
            阿拉尔
          </div>
          <div class="item">
            阿拉尔
          </div>
        </div>
      </div>
      <div class="area">
        <div class="title">A</div>
        <div class="item-list">
          <div class="item">
            阿拉尔
          </div>
          <div class="item">
            阿拉尔
          </div>
          <div class="item">
            阿拉尔
          </div>
          <div class="item">
            阿拉尔
          </div>
          <div class="item">
            阿拉尔
          </div>
          <div class="item">
            阿拉尔
          </div>
          <div class="item">
            阿拉尔
          </div>
        </div>
      </div>
      <div class="area">
        <div class="title">A</div>
        <div class="item-list">
          <div class="item">
            阿拉尔
          </div>
          <div class="item">
            阿拉尔
          </div>
          <div class="item">
            阿拉尔
          </div>
          <div class="item">
            阿拉尔
          </div>
          <div class="item">
            阿拉尔
          </div>
          <div class="item">
            阿拉尔
          </div>
          <div class="item">
            阿拉尔
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import BScroll from 'better-scroll'
export default {
  name: 'CityList',
  mounted () {
    this.scroll = new BScroll(this.$refs.wrapper)
  }
}
</script>
<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .list
    overflow :hidden
    position:absolute
    top:1.58rem
    left:0
    right:0
    bottom:0
    .title
      line-height:.44rem
      background:#eee
      font-size :.26rem
      padding-left:.2rem
      color:#666
    .button-list
      overflow :hidden
      padding: .1rem .6rem .1rem .1rem
      .button-wrapper
        float:left
        width:33.33%
        .button
          text-align :center
          padding: .1rem 0
          border-radius: .06rem
          margin:.1rem
          border:.02rem solid #ccc
    .item-list
      .item
        line-height :.76rem
        padding-left:.2rem
        border-bottom :.02rem solid #ccc
</style>