<template>
  <div>
    <div class="recommend-title">周末去哪儿</div>
      <ul>
        <li class="item border-bottom"  v-for="item of recommendList" :key="item.id">
          <div class="item-img-wrapper">
            <img class="item-img" :src="item.imgUrl" alt="">
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
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1603/89/a64d5966351b04.jpg_r_640x214_45776b4c.jpg',
        title: '云台山',
        desc: '国家5A级景区国家5A级景区国家5A级景区国家5A级景区国家5A级景区国家5A级景区'
      },{
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1603/89/a64d5966351b04.jpg_r_640x214_45776b4c.jpg',
        title: '云台山',
        desc: '国家5A级景区国家5A级景区国家5A级景区国家5A级景区国家5A级景区国家5A级景区'
      },{
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1603/89/a64d5966351b04.jpg_r_640x214_45776b4c.jpg',
        title: '云台山',
        desc: '国家5A级景区国家5A级景区国家5A级景区国家5A级景区国家5A级景区国家5A级景区'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .recommend-title
    margin-top :.2rem
    line-height .8rem
    background #eee
    text-indent .2rem
  .item-img-wrapper
    overflow :hidden
    padding-bottom :33.9%
    height:0
    .item-img
      width:100%
  .item-info
    padding:.1rem
    .item-title
      line-height:.54rem
      font-size: .32rem
      ellipsis()
    .item-desc
      line-height .4rem
      color: gray
      ellipsis()
</style>
