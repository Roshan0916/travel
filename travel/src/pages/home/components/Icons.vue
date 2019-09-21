<template>
  <div class="icons">
    <swiper>
       <swiper-slide v-for="(page, index) of pages" :key="index">
          <div class="icon" v-for="item in page" :key="item.id">
            <div class="icon-img">
              <img class="icon-img-content"
              :src="item.imgUrl"/>
            </div>
            <p class="icon-desc">{{item.desc}}</p>
          </div>
       </swiper-slide>
    </swiper>
  </div>
</template>
<script>
export default {
  name:'HomeIcons',
  data () {
    return {
      iconList: [{
        id: '0001',
        imgUrl: 'https://imgs.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        desc:'热门景点'
      },{
        id: '0002',
        imgUrl: 'https://imgs.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        desc:'热门景点'
      }]
    }
  },
  computed:{
    pages () {
      const pages = []
      this.iconList.forEach((item,index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]){
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>
<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  @import '~styles/mixins.styl'
  .icons >>> .swiper-container
    height: 0
    padding-bottom: 50%
  .icons
    margin-top:.1rem
    .icon
      float:left
      position:relative
      overflow:hidden
      width:25%
      padding-bottom:25%
      .icon-img
        position:absolute
        top:0
        left:0
        right:0
        bottom 0.44rem
        .icon-img-content
          display:block
          margin:0 auto
          height: 100%
      .icon-desc
        width:100%
        text-align:center
        position:absolute
        bottom:0
        line-height 0.44rem
        color: $darkTextColor
        ellipsis()
</style>