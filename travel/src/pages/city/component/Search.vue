<template>
  <div class="serach">
    <input class="search-input" type="text" placeholder="输入城市或者拼音" />
  </div>
</template>

<script>
export default {
  name: 'CitySearch'
}
</script>

<style lang="stylus" scoped>
  @import '~styles/variables.styl'
  .serach
    height: .72rem
    padding: 0 .1rem
    background: $bgColor
    text-align: center
    .search-input
      box-sizing: border-box
      padding: 0 .1rem
      width: 100%
      height: .62rem
      line-height: .62rem
      text-align: center
      border-radius: .06rem
      color: #666
</style>
