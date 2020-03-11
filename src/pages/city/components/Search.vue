<template>
  <div class="search">
    <input class="search-input" type="text" placeholder="输入城市名或拼音" />
  </div>
</template>

<script>
export default {
  name: 'CitySearch'
}
</script>

<style lang="stylus" scoped>
  @import '~styles/variable.styl'
  .search
    height: 2rem
    padding: 0 .2rem
    margin: 0
    background: $bgColor
    .search-input
      box-sizing: border-box
      width: 100%
      height: 1.62rem
      line-height: 1.62rem
      padding: 0 .2rem
      text-align: center
      border-radius: .06rem
      outline: none
      border: 0
      color: #666
</style>