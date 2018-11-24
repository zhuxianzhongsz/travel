<template>
  <div>
    <div class="title">热门榜单</div>
    <ul>
      <router-link tag="li" class="item border-bottom" v-for="item of list" :key="item.id" :to="'/detail/' + item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl">
        </div>
        <div class="item-info">
          <p class="item-title">{{ item.title }}</p>
          <p class="item-desc">{{ item.desc }}</p>
          <button class="item-button">查看详情</button>
        </div>
      </router-link>
    </ul>
  </div>
</template>
<script>
export default {
  name: 'HomeRecommend',
  props: {
    list: Array
  },
  data () {
    return {
      // recommendList: [
      //   { id: '0001', imgUrl: 'http://img1.qunarzz.com/sight/p0/201405/30/a9edfcb4fe0e119da480d30d22ade127.jpg_200x200_6af441cf.jpg', title: '地王大厦', desc: '俯仰百年都市风光，远眺南明珠秀色。' },
      //   { id: '0002', imgUrl: 'http://img1.qunarzz.com/sight/p0/201405/30/a9edfcb4fe0e119da480d30d22ade127.jpg_200x200_6af441cf.jpg', title: '地王大厦', desc: '俯仰百年都市风光，远眺南明珠秀色。' },
      //   { id: '0003', imgUrl: 'http://img1.qunarzz.com/sight/p0/201405/30/a9edfcb4fe0e119da480d30d22ade127.jpg_200x200_6af441cf.jpg', title: '地王大厦', desc: '俯仰百年都市风光，远眺南明珠秀色。' }
      // ]
    }
  }
}
</script>
<style lang="stylus" scoped>
  @import '~styles/mixin.styl'
  .title
    margin-top: .2rem
    line-height: .8rem
    background: #eee
    text-indent: .2rem
  .item
    overflow: hidden
    display: flex
    height: 1.9rem
    .item-img
      width: 1.7rem
      height: 1.7rem
      padding: .1rem
    .item-info
      flex: 1
      padding: .1rem
      min-width: 0
      .item-title
        line-height: .5rem
        font-size: .32rem
        color: #212121
        ellipsis()
      .item-desc
        line-height: .6rem
        color: #616161
        ellipsis()
      .item-button
        margin-top: .18rem
        line-height: .44rem
        background: #ff9300
        padding: 0 .2rem
        border-radius: .06rem
        color: #fff
</style>
