<template>
  <div>
    <div class="title">周末去哪玩</div>
    <ul>
      <li
        class="item border-bottom"
        v-for="item of weekendList"
        :key="item.id"
      >
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl" />
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
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
      weekendList: [{
        id: '1',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1511/2b/5e0923cd15e06.jpg_r_640x214_b9c024c1.jpg',
        title: '细数石家庄温泉',
        desc: '石家庄有没有让你心动的温泉'
      }, {
        id: '2',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1507/82/06e79c5f8d6e7.jpg_r_640x214_5e63707e.jpg',
        title: '当地人玩什么',
        desc: '石家庄人民周末好玩法'
      }, {
        id: '3',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1703/e1/93571b553ed1aa.jpg_r_640x214_a7c8c3f6.jpg',
        title: '风景胜地',
        desc: '快来一睹河北风光'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .title
    line-height: .8rem
    background: #eee
    text-indent: .2rem
  .item-img-wrapper
    overflow: hidden
    height: 0
    padding-bottom: 37.09%
    .item-img
      width: 100%
  .item-info
    padding: .1rem
    .item-title
      line-height: .54rem
      font-size: .32rem
      ellipsis()
    .item-desc
      line-height: .4rem
      color: #ccc
      ellipsis()
</style>
