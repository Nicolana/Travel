<template>
  <div>
    <div class="recommend-title">周末去哪儿</div>
    <ul class="item-init">
      <li class="item border-bottom" v-for="item of list" :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl" />
        </div>
        <div class="item-info">
          <p class="item-title">{{ item.title }}</p>
          <p class="item-desc">
            {{ item.desc }}
          </p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
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
  .item-img-wrapper
    overflow: hidden
    height: 0
    padding-bottom: 50%
    .item-img
      width: 100%
  .item-info
    padding: .1rem
    margin-left: .2rem
    margin-right: .3rem
    // min-width: 0
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
      margin-bottom: .5rem
      padding: 0
      ellipsis()

</style>
