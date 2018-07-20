<template>
  <div>
    <div class="titles">周末去哪儿</div>
    <ul>
      <li class="item" v-for="item in weekList" :key="item.id">
        <div class="item-img">
          <img :src="item.imgUrl"/>
        </div>
        <div class="item-content">{{item.name}}</div>
        <div class="item-desc">{{item.desc}}</div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekfly',
  data () {
    return {
      weekList: [
        {
          id: '0001',
          name: '杭州必游top10',
          desc: '杭州，前世今生与你有一场美丽约会',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1505/9f/7d45cc38259e0.jpg_r_640x214_156f4299.jpg'
        },
        {
          id: '0002',
          name: '杭州必游top10',
          desc: '杭州，前世今生与你有一场美丽约会',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1505/9f/7d45cc38259e0.jpg_r_640x214_156f4299.jpg'
        },
        {
          id: '0003',
          name: '杭州必游top10',
          desc: '杭州，前世今生与你有一场美丽约会',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1505/9f/7d45cc38259e0.jpg_r_640x214_156f4299.jpg'
        },
        {
          id: '0004',
          name: '杭州必游top10',
          desc: '杭州，前世今生与你有一场美丽约会',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1505/9f/7d45cc38259e0.jpg_r_640x214_156f4299.jpg'
        },
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import "~styles/minnis.styl"
  .titles
    margin-top: .2rem
    line-height: .47rem
    background: #eee
    text-indent: .2rem
  .imgs
    overflow: hidden
    height: 0
    padding-bottom: 33.4375%
    .img-desc
      width: 100%
  .item
    position: relative;
    margin-bottom: .1rem;
    background: #fff;
    min-width 0
    .item-content
      overflow: hidden;
      padding-left: .26rem
      color: #212121;
      font-size: .28rem;
      line-height: .48rem;
      white-space: nowrap;
      ellipse()
    .item-desc
      overflow: hidden
      line-height: .42rem
      margin-top: .08rem
      margin-bottom: .2rem
      color: #cccccc
      padding-left: .26rem
      ellipse()
    .item-img
      overflow: hidden
      height: 0
      padding-bottom: 36.8550%
</style>
