<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe743;</div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe7b3;</span>
      输入城市/景点/地点
    </div>
    <div class="header-right">
    城市
      <span class="iconfont arrow-icon">&#xe64a;</span>

    </div>
  </div>
</template>

<script>
export default{
  name: 'HomeHeader'
}
</script>

<style lang="stylus" scoped>
  @import '~styles/variable.styl'
  .header
    display: flex
    line-height:2.86rem
    background: $bgColor
    color: #fff
    font-size: .9rem
    .header-left
      width: 2.64rem
      float: left
      .back-icon
        text-align: center
        font-size: 1.7rem
    .header-input
      flex: 1
      background: #fff
      margin-top: .52rem
      margin-left: .2rem
      border-radius: .1rem
      line-height: 1.9rem
      height: 1.9rem
      color: #ccc
      padding-left: .4rem
      // font-size: 1rem
      // vertical-align: middle
      // .iconfont
      //   font-size: 1.2rem
    .header-right
      width: 3.34rem
      float: right
      text-align: center
      margin-left: .6rem
      margin-right: .6rem
      .arrow-icon
        font-size: .9rem
</style>
