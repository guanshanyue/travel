<template>
  <div>
    <home-header :city="city"></home-header>
    <home-swiper :swiperList="swiperList"></home-swiper>
    <home-icons :iconList="iconList"></home-icons>
    <home-recommand :recommend="recommend"></home-recommand>
    <home-weekfly :weekendList="weekendList"></home-weekfly>
  </div>
</template>

<script>
import HomeHeader from './component/Header'
import HomeSwiper from './component/Swiper'
import HomeIcons from './component/Icons'
import HomeRecommand from './component/Recommand'
import HomeWeekfly from './component/Weekfly'
import axios from 'axios'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeRecommand,
    HomeWeekfly
  },
  data () {
    return {
      city: '',
      swiperList: [],
      iconList: [],
      recommend: [],
      weekendList: []
    }
  },
  methods: {
    getHomeinfo () {
      axios.get('/api/index.json')
        .then(this.getHomeinfoSucc)
    },
    getHomeinfoSucc (res) {
      res = res.data
      if (res.ret && res.data) {
        const data = res.data
        this.city = data.city
        this.swiperList = data.swiperList
        this.iconList = data.iconList
        this.recommend = data.recommendList
        this.weekendList = data.weekendList
      }
    }
  },
  mounted () {
    this.getHomeinfo()
  }
}
</script>

<style scoped>
</style>
