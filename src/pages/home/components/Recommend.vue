<template>
  <div>
    <div class="recommend-title">推荐栏目</div>
    <ul class="item-init">
      <li class="item border-bottom" v-for="item of list" :key="item.id">
          <img class="item-img" :src="item.imgUrl" />
        <div class="item-info">
          <p class="item-title">{{ item.title }}</p>
          <p class="item-desc">
            {{ item.desc }}
          </p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  props: {
    list: Array
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/variable.styl'
  @import '~styles/mixins.styl'
  .recommend-title
    line-height: 2.2rem
    background: #ccc
    text-indent: 1.2rem
    color: $darkTextColor
  .item
    overflow: hidden
    display: flex
    height: 5rem
    .item-img
      width: 4.7rem
      height: 4.7rem
      padding: .1rem
    .item-info
      flex: 1
      padding: .1rem
      margin-left: .2rem
      margin-right: .3rem
      min-width: 0
      .item-title
        line-height: .84rem
        font-size: .82rem
        margin-top: .3rem
        margin-bottom: 0
        padding: 0
        ellipsis()
      .item-desc
        line-height: .9rem
        color: #ccc
        margin-top: .5rem
        margin-bottom: 0
        padding: 0
        ellipsis()
      .item-button
        border: 1px solid transparent
        line-height: .84rem
        margin-top: .56rem
        background: #ff9300
        outline: none
        padding: .2rem
        border-radius: .1rem
        color: #fff
</style>
