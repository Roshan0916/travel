<template>
<div class="wrapper">
<swiper :options="swiperOption">
    <!-- slides -->
    <swiper-slide v-for="item of swiperList" :key="item.id">
      <img class="swiper-img" :src="item.imgUrl" />
    </swiper-slide>
    <!-- Optional controls -->
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
</div>
</template>
<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id:'0001',
        imgUrl:'https://imgs.qunarzz.com/piao/fusion/1609/4d/3dc09bcc290f0c02.jpg_750x200_09c97d67.jpg'
      },{
        id:'0002',
        imgUrl:'https://imgs.qunarzz.com/piao/fusion/1609/4d/3dc09bcc290f0c02.jpg_750x200_09c97d67.jpg'
      }]
    }
  }
}
</script>
<style lang='stylus' scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background: #fff
  .wrapper
    overflow: hidden
    width: 100%
    height: 0
    padding-bottom: 27.5%
    background : #eee
    .swiper-img
      width:100%
</style>
