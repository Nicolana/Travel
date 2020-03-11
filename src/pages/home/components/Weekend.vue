<template>
  <div>
    <div class="recommend-title">周末去哪儿</div>
    <ul class="item-init">
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
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
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'https://imgs.qunarzz.com/vs_ceph_vs_tts/0abd521e-2de6-4fdf-86a9-cc6c49f6470a.jpg_r_480x320x90_7aa00bcd.jpg',
        title: '重庆-土耳其 10天跟团游',
        desc: '错峰钜惠！早订享立减💎蓝色土耳其深度10-12日，洞穴酒店，热气球圣地'
      }, {
        id: '0002',
        imgUrl: 'https://imgs.qunarzz.com/vs_ceph_vs_tts/bd85c7f2-f8ee-431d-bed8-46c453bce728.jpg_r_480x320x90_0fd45f3a.jpg',
        title: '成都-巴厘岛 7天6晚跟团游',
        desc: '顶奢迪拜，品质7日🔥豪华四星酒店，打卡棕榈岛+哈利法塔，赠送旅游人身意外险'
      }]
    }
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
