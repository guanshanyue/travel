<template>
  <div>
    <div class="titles">热门推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item in recommend" :key="item.id">
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
  props: {
    recommend: Array
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
