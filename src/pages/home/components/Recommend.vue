<template>
  <div>
      <div class="recommend-title">热销推荐</div>
      <ul>
        <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
          <img class="item-img" :src="item.imgUrl" alt="">
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
        id: '0001',
        imgUrl: 'https://hbimg.huabanimg.com/500960e9743c12e2762667a06ff78ac0d03a634f20a51-zsfAb7_fw236',
        title: '这里是title这里是title',
        desc: '这里是描述，描述'
      }, {
        id: '0002',
        imgUrl: 'https://hbimg.huabanimg.com/500960e9743c12e2762667a06ff78ac0d03a634f20a51-zsfAb7_fw236',
        title: '这里是title这里是title',
        desc: '这里是描述，描述'
      }, {
        id: '0003',
        imgUrl: 'https://hbimg.huabanimg.com/500960e9743c12e2762667a06ff78ac0d03a634f20a51-zsfAb7_fw236',
        title: '这里是title这里是title',
        desc: '这里是描述，描述'
      }]
    }
  }
}
</script>
<style lang="stylus" scoped>
@import '~styles/mixins.styl';
  .recommend-title
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
        ellipisis()
      .item-desc
        line-height: .4rem
        color: #ccc
        ellipisis()
      .item-button
        line-height: .44rem
        margin-top: .16rem
        background: #ff9300
        padding: 0 .2rem
        border-radius .06rem
        color: #ffffff
</style>
