<template>
    <div class="icon">
      <div class="icon-content">
        <div class="icon-content-img">
          <img class="icon-content-img-content" src="http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png"/>
        </div>
        <div class="icon-content-text">景点门票</div>
      </div>
      <div class="icon-content">
        <div class="icon-content-img">
          <img class="icon-content-img-content" src="http://img1.qunarzz.com/piao/fusion/1804/ed/cf572be30fc32f02.png"/>
        </div>
        <div class="icon-content-text">Q+精选</div>
      </div>
      <div class="icon-content">
        <div class="icon-content-img">
          <img class="icon-content-img-content" src="http://img1.qunarzz.com/piao/fusion/1803/47/c2b659e048b11602.png"/>
        </div>
        <div class="icon-content-text">主题乐园</div>
      </div>
      <div class="icon-content">
        <div class="icon-content-img">
          <img class="icon-content-img-content" src="http://img1.qunarzz.com/piao/fusion/1803/75/eca3ce656c886502.png"/>
        </div>
        <div class="icon-content-text">漂流</div>
      </div>
      <div class="icon-content">
        <div class="icon-content-img">
          <img class="icon-content-img-content" src="http://img1.qunarzz.com/piao/fusion/1803/17/99402a22ce4af302.png"/>
        </div>
        <div class="icon-content-text">西湖</div>
      </div>
      <div class="icon-content">
        <div class="icon-content-img">
          <img class="icon-content-img-content" src="http://img1.qunarzz.com/piao/fusion/1803/6a/45f595250c73d102.png"/>
        </div>
        <div class="icon-content-text">夏日玩水</div>
      </div>
      <div class="icon-content">
        <div class="icon-content-img">
          <img class="icon-content-img-content" src="http://img1.qunarzz.com/piao/fusion/1803/e3/67df61427c8e1302.png"/>
        </div>
        <div class="icon-content-text">宋城千古情</div>
      </div>
      <div class="icon-content">
        <div class="icon-content-img">
          <img class="icon-content-img-content" src="http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png"/>
        </div>
        <div class="icon-content-text">杭州必游</div>
      </div>
    </div>
</template>

<script>
export default {
  name: 'HomeIcons'
}
</script>

<style lang="stylus" scoped>
  @import "~styles/variables.styl"
  .icon
    overflow: hidden
    height: 0
    width: 100%
    padding-bottom: 50%
    /*background: black*/
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
</style>
