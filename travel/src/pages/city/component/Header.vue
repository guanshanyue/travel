<template>
  <div class="header">
    <span>城市选择</span>
      <div class="header-left">
        <router-link to="/">
          <div class="iconfont base-icon">&#xe624;</div>
        </router-link>
      </div>
  </div>
</template>

<script>
export default {
  name: 'CityHeader'
}
</script>

<style lang="stylus" scoped>
  @import '~styles/variables.styl'
  .header
    overflow: hidden
    height: $HeaderHeight
    line-height: $HeaderHeight
    color: #ffffff
    background: $bgColor
    text-align: center
    font-size: .32rem
    .header-left
      width : .64rem
      float: left
     .base-icon
        text-align: center
        font-size: .4rem
        color: #ffffff
</style>
