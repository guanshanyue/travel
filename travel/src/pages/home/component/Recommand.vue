<template>
  <div>
    <div class="titles">热门推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item in recommand" :key="item.id">
        <img class="item-img" :src="item.imgUrl"/>
        <div class="item-info">
          <p class="item-info-p1">{{item.name}}</p>
          <p class="item-info-p2">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommand',
  data () {
    return {
      recommand: [
        {
          id: '0001',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1607/7c/7cda8b6782dabd80b4.img.jpg_200x200_2039e660.jpg',
          name: '上海迪士尼乐园',
          desc: '查看详情'
        },
        {
          id: '0002',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1607/7c/7cda8b6782dabd80b4.img.jpg_200x200_2039e660.jpg',
          name: '上海迪士尼乐园',
          desc: '查看详情'
        },
        {
          id: '0003',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1607/7c/7cda8b6782dabd80b4.img.jpg_200x200_2039e660.jpg',
          name: '上海迪士尼乐园',
          desc: '查看详情'
        },
        {
          id: '0004',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1607/7c/7cda8b6782dabd80b4.img.jpg_200x200_2039e660.jpg',
          name: '上海迪士尼乐园',
          desc: '查看详情'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
  //@import "~styles/minnis.styl"
  @import "~styles/minnis.styl"
  .titles
    margin-top: .2rem
    line-height: .47rem
    background: #eee
    text-indent: .2rem
  .item
    overflow hidden
    display flex
    height 1.9rem
    .item-img
      height: 1.7rem
      width 1.7rem
      padding .1rem
    .item-info
      flex: 1
      padding: .1rem
      min-width 0
      .item-info-p1
        line-height .54rem
        font-size: .32rem
        ellipse()
      .item-info-p2
        line-height .4rem
        color: #cccccc
        ellipse()
      .item-button
        line-height .44rem
        margin-top: .16rem
        background: #ff9300
        color: #333333
        padding: 0 .2rem
        border-radius: .06rem
</style>
