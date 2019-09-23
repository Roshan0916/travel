<template>
  <div>
    <detail-banner></detail-banner>
    <detail-header></detail-header>
    <div class="content">
      <detail-list :list="list"></detail-list>
    </div>
  </div>
</template>
<script>
import DetailBanner from './components/Banner'
import DetailHeader from './components/Header'
import DetailList from './components/List'
export default {
  name: 'Detail',
  components: {
    DetailBanner,
    DetailHeader,
    DetailList
  },
  data () {
    return {
      list: [{
        title: '成ren票',
        children:[{
          title:'成人三馆联票',
          children:[{
            title:'成人三观联票第五售票处'
          }]
        }]
      },
      {
        title: '成ren票'
      },
      {
        title: '成ren票'
      },
      {
        title: '成ren票'
      }]
    }
  }
}
</script>
<style lang="stylus" scoped>
  .content
    height:15rem

</style>