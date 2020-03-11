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
  data () {
    return {
      iconList: [{
        id: '0001',
        imgUrl: require('@/assets/icons/canju.png'),
        desc: '餐具'
      }, {
        id: '0002',
        imgUrl: require('@/assets/icons/maojin.png'),
        desc: '毛巾'
      }, {
        id: '0003',
        imgUrl: require('@/assets/icons/baobei.png'),
        desc: '宝贝'
      }, {
        id: '0004',
        imgUrl: require('@/assets/icons/naizui.png'),
        desc: '奶嘴'
      }, {
        id: '0005',
        imgUrl: require('@/assets/icons/shijin.png'),
        desc: '湿巾'
      }, {
        id: '0006',
        imgUrl: require('@/assets/icons/sushenyi.png'),
        desc: '塑身衣'
      }, {
        id: '0007',
        imgUrl: require('@/assets/icons/xiaofangjin.png'),
        desc: '小方巾'
      }, {
        id: '0008',
        imgUrl: require('@/assets/icons/yingerche.png'),
        desc: '婴儿车'
      }, {
        id: '0009',
        imgUrl: require('@/assets/icons/yugang.png'),
        desc: '浴缸'
      }]
    }
  },
  computed: {
    pages () {
      const pages = []
      this.iconList.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
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
