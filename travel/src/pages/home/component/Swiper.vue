<template>
  <div class="swiper-wapper">
    <swiper :options="swiperOption" v-if="showSwiper">
      <!-- slides -->
      <swiper-slide v-for="item in this.swiperList" :key="item.id" >
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
  props: {
    swiperList: Array
  },
  data: function () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      }
    }
  },
  computed: {
    showSwiper () {
      return this.swiperList.length
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
