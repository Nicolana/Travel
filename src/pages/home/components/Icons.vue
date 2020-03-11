<template>
  <div class="icons">
      <swiper>
        <swiper-slide v-for="(page, index) of pages" :key="index">
          <div class="icon" v-for="icon of page" :key="icon.id">
            <div class="icon-img">
              <img class="icon-img-content" :src="icon.imgUrl">
            </div>
            <p class="icon-desc">{{icon.desc}}</p>
          </div>
        </swiper-slide>
      </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  props: {
    list: Array
  },
  computed: {
    pages () {
      const pages = []
      this.list.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    },
    showIcons () {
      return this.list.length
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  @import '~styles/variable.styl'
  .icons >>> .swiper-container
    height: 0
    padding-bottom: 50%
  .icons
    margin-top: .5rem
    .icon
      position: relative
      overflow: hidden
      float: left
      width: 25%
      height: 0
      padding-bottom: 25%
      .icon-img
        position: absolute
        top: 0
        left: 0
        right: 0
        bottom: 1.44rem
        box-sizing: border-box
        padding: .1rem
        .icon-img-content
          display: block
          margin: 0 auto
          height: 65%
      .icon-desc
        position: absolute
        left: 0
        right: 0
        bottom: 0
        height: .84rem
        line-height: .84rem
        text-align: center
        color: $darkTextColor
        ellipsis()
</style>
