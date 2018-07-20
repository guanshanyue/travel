<template>
  <div>
    <home-header></home-header>
    <home-swiper></home-swiper>
    <home-icons></home-icons>
    <home-recommand></home-recommand>
    <home-weekfly></home-weekfly>
  </div>
</template>

<script>
import HomeHeader from './component/Header'
import HomeSwiper from './component/Swiper'
import HomeIcons from './component/Icons'
import HomeRecommand from './component/Recommand'
import HomeWeekfly from './component/Weekfly'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeRecommand,
    HomeWeekfly
  }
}
</script>

<style scoped>
</style>
