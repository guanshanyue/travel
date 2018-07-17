<template>
  <div class="swiper-wapper">
    <swiper :options="swiperOption">
      <!-- slides -->
      <swiper-slide v-for="item in swiperList" :key="item.id" >
        <img class="swiper-img" :src="item.imgUrl"/>
      </swiper-slide>
      <!-- Optional controls -->
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data: function () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [
        {
          id: '001',
          imgUrl: 'https://imgs.qunarzz.com/piao/fusion/1804/bd/8e4a1c3f470d3702.jpg_750x200_f1f0a8c7.jpg'
        },
        {
          id: '002',
          imgUrl: 'https://imgs.qunarzz.com/piao/fusion/1807/c6/44fce1467be17702.jpg_750x200_406f5fc3.jpg'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .swiper-wapper >>> .swiper-pagination-bullet-active
    background: #ffffff
  .swiper-wapper
    overflow: hidden
    width: 100%
    height: 0
    padding-bottom: 26.66%
    .swiper-img
      width: 100%
</style>
