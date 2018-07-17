<template>
    <div class="icon swiper-wapper">
      <swiper>
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
  data () {
    return {
      imgList: [
        {
          id: '0001',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
          desc: '景点门票'
        },
        {
          id: '0002',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png',
          desc: '一日游'
        },
        {
          id: '0003',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/47/c2b659e048b11602.png',
          desc: '主题乐园'
        },
        {
          id: '0004',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/75/eca3ce656c886502.png',
          desc: '漂流'
        },
        {
          id: '0005',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
          desc: '西湖'
        },
        {
          id: '0006',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/6a/45f595250c73d102.png',
          desc: '夏日玩水'
        },
        {
          id: '0007',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
          desc: '景点门票7'
        },
        {
          id: '0008',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/e3/67df61427c8e1302.png',
          desc: '宋城千古情'
        },
        {
          id: '0009',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png',
          desc: '杭州必游'
        }
      ]
    }
  },
  computed: {
    pages: function () {
      const pages = []
      this.imgList.forEach((item, index) => {
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
