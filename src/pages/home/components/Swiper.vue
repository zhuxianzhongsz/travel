<template>
  <div class="wrapper">
    <swiper :options="swiperOption" v-if="list.length">
      <swiper-slide v-for="item of list" :key="item.id" :data-swiper-autoplay='3500'>
        <img class="swiper-img" :src="item.imgUrl" />
      </swiper-slide>
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
  </div>
</template>
<script>
export default {
  name: 'HomeSwiper',
  props: {
    list: Array
  },
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true,
        autoplay: true,
        speed: 400,
        autoplayDisableOnInteraction: false
      },
      swiperList: [
        // { id: '0001', imgUrl: 'http://img1.qunarzz.com/piao/fusion/1807/66/e5a5cec881702f02.jpg_750x200_67bb5691.jpg' },
        // { id: '0002', imgUrl: 'http://img1.qunarzz.com/piao/fusion/1808/8a/1957a0fb58ad0402.jpg_750x200_e72b8c0f.jpg' },
        // { id: '0003', imgUrl: 'http://img1.qunarzz.com/piao/fusion/1808/59/371af39a4ca5702.jpg_750x200_1a9cfe57.jpg' },
        // { id: '0004', imgUrl: 'https://img1.qunarzz.com/piao/fusion/1808/fd/fddc5309111a0402.jpg_750x200_e7b93551.jpg' },
        // { id: '0005', imgUrl: 'http://img1.qunarzz.com/piao/fusion/1805/e8/14b75b1c81fbe702.jpg_750x200_e6d4f1f1.jpg' }
      ]
    }
  }
}
</script>
<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background-color:#fff
  .wrapper
    overflow: hidden
    width: 100%
    height: 0
    padding-bottom:26%
    .swiper-img
      width:100%
    .swiper-pagination
      margin-bottom:10px
</style>
