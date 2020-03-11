<template>
  <div>
    <div class="recommend-title">推荐栏目</div>
    <ul class="item-init">
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
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
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1411/34/6aec007588037c2d9ef339d81aeba256.water.jpg_256x160_ec997312.jpg',
        title: '重庆-土耳其 10天跟团游',
        desc: '错峰钜惠！早订享立减💎蓝色土耳其深度10-12日，洞穴酒店，热气球圣地'
      }, {
        id: '0002',
        imgUrl: 'http://imgs.qunarzz.com/p/tts2/1708/66/62a51d0822609f02.jpg_r_480x320x90_df7e7c29.jpg',
        title: '重庆-迪拜，7天跟团游',
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
