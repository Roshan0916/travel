<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
          <img class="item-img" :src="item.imgUrl" />
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  name: 'HomeRecommmend',
  data () {
    return{
      recommendList:[{
      id: '0001',
      imgUrl:'https://imgs.qunarzz.com/sight/p0/1901/8c/8c1d317bc954ce06a3.water.jpg_200x200_94fd133d.jpg',
      title: '标题1',
      desc: '内容啊'
    },{
      id: '0002',
      imgUrl:'https://imgs.qunarzz.com/sight/p0/1901/8c/8c1d317bc954ce06a3.water.jpg_200x200_94fd133d.jpg',
      title: '标题1',
      desc: '内容啊'
    }]
    }
  }
    
}
</script>
<style lang="stylus" scoped>
@import '~styles/mixins.styl'
  .title
    line-height: .8rem
    background: #eee
    text-indent: .2rem
    margin-top:.2rem
  .item
    overflow:hidden
    display:flex
    height 1.9rem
    .item-img
      width:1.7rem
      height 1.7rem
      padding:.1rem
    .item-info
      flex:1
      padding:.1rem
      min-width:0
      .item-title
        line-height:.54rem
        font-size:.32rem
        ellipsis()
      .item-desc
        line-height:.4rem
        color:#ccc
        ellipsis()
      .item-button
        background :#ff9300
        padding :0 .2rem
        border-radius:.06rem
        margin-top:.3rem
</style>