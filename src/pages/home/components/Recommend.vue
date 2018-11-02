<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li
        class="item border-bottom"
        v-for="item of recommendList"
        :key="item.key">
        <img class="item-img" :src='item.imgUrl' />
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
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
        id: '1',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1607/c3/c3dae954f5da5a20a3.water.jpg_200x200_9ef2b3c0.jpg',
        title: '石家庄海悦天地海洋公园',
        desc: '可订明日'
      },
      {
        id: '2',
        imgUrl: 'http://img1.qunarzz.com/sight/p95/201211/03/30f3d57d7f4d4e4a93835fbb.jpg_200x200_f3d8cf9f.jpg',
        title: '石家庄市动物园',
        desc: '可订明日'
      },
      {
        id: '3',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1509/d3/d3e80935a714d3b4.img.jpg_200x200_86fabdf7.jpg',
        title: '石家庄植物园',
        desc: '随买随用'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .title
    margin-top: .2rem
    line-height: .8rem
    background: #eee
    text-indent: .2rem
  .item
    overflow: hidden
    display: flex
    height: 1.9rem
    .item-img
      width: 1.7rem
      height: 1.7rem
      padding: .1rem
    .item-info
      flex: 1
      padding: .1rem
      min-width: 0
      .item-title
        line-height: .54rem
        font-size: .32rem
        ellipsis()
      .item-desc
        line-height: .4rem
        color: #ccc
        ellipsis()
      .item-button
        line-height: .44rem
        margin-top: .16rem
        background: #ff9300
        padding: 0 .2rem
        border-radius: .06rem
        color: #fff
</style>
