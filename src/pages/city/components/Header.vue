<template>
  <div class="header">
    城市选择
    <router-link to="/">
    <div class="iconfont header-back">&#xe743;</div>
  </router-link>
  </div>
</template>
<script>
export default {
  name: 'CityHeader'
}
</script>
<style lang="stylus" scoped>
  @import '~styles/variable.styl'
  .header
    position: relative
    overflow: hidden
    background: $bgColor
    line-height: $headerHeight
    height: $headerHeight
    text-align: center
    color: #fff
    font-size: 15px
    .header-back
      position: absolute
      top: 0
      left: 0
      width: 2.64rem
      text-align: center
      font-size: 1.7rem
      color: #fff
</style>
