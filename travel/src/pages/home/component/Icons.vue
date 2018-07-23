<template>
    <div class="icon swiper-wapper">
      <swiper :options="swiperOption">
        <swiper-slide v-for="(page,index) in pages" :key="index">
          <div class="icon-content" v-for="item in page" :key="item.id">
            <div class="icon-content-img">
              <img class="icon-content-img-content" :src="item.imgUrl"/>
            </div>
            <div class="icon-content-text">{{item.desc}}</div>
          </div>
        </swiper-slide>
      </swiper>
    </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  props: {
    iconList: Array
  },
  data () {
    return {
      swiperOption : {
        autoplay: false
      }
    }
  },
  computed: {
    pages: function () {
      const pages = []
      this.iconList.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
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
  @import "~styles/variables.styl"
  @import "~styles/minnis.styl"
  .icon >>> .swiper-container
    height: 0
    padding-bottom: 50%
  .icon-content
    position: relative
    overflow: hidden
    float: left
    height: 0
    width: 25%
    padding-bottom: 25%
    /*background: blue*/
    .icon-content-img
      position: absolute
      top: 0
      left: 0
      right: 0
      bottom: .44rem
      box-sizing: border-box
      padding: .1rem
      /*background: red*/
      .icon-content-img-content
        display: block
        margin: 0 auto
        height: 100%
    .icon-content-text
      position: absolute
      left: 0
      right: 0
      bottom: 0
      line-height: .44rem
      height: .44rem
      text-align: center
      color: $fontColor
      ellipse()
</style>
