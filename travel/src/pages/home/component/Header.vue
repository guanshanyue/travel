<template>
    <div class="header">
      <div class="header-left">
        <div class="iconfont base-icon">&#xe624;</div>
      </div>
      <div class="header-input">
        <span class="iconfont">&#xe632;</span>
        输入城市/景点/游玩主题
      </div>
      <router-link to="/city">
        <div class="header-right">
          {{city}}
          <span class="iconfont atter-icon">&#xe600;</span>
        </div>
      </router-link>
    </div>
</template>

<script>
export default {
  name: 'HomeHeader',
  props: {
    city: String
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/variables.styl'
  .header
    line-height: $HeaderHeight
    display: flex
    background: $bgColor
    color: #ffffff
  .header-left
    width : .64rem
    float: left
    .base-icon
      text-align: center
      font-size: .4rem
  .header-input
    flex: 1
    height: .64rem
    line-height: .64rem
    margin-top: .12rem
    margin-left: .2rem
    background: #ffffff
    border-radius: .2rem
    padding-left: .2rem
    color: #cccccc
  .header-right
    width: 1.24rem
    float: right
    text-align: center
    color: #ffffff
    .atter-icon
      font-size: .2rem
      margin-left: -.04rem
</style>
