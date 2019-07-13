<template>
  <div>
      <div class="recommend-title">周末去哪儿</div>
      <ul>
        <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
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
        imgUrl: 'https://hbimg.huabanimg.com/70c554033a25af88df214e5efe153448c08955bf14e1e-7y95bI_fw236',
        title: '这里是title这里是title',
        desc: '这里是描述，描述'
      }, {
        id: '0002',
        imgUrl: 'https://hbimg.huabanimg.com/f7e7d8712ff9f77e9cf77a75b6a22f3c5e8c552716f9b-YizPZU_fw236',
        title: '这里是title这里是title',
        desc: '这里是描述，描述'
      }, {
        id: '0003',
        imgUrl: 'https://hbimg.huabanimg.com/f7e7d8712ff9f77e9cf77a75b6a22f3c5e8c552716f9b-YizPZU_fw236',
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
  .item-img-wrapper
    overflow: hidden
    height: 0
    padding-bottom: 33.9%
    .item-img
      width: 100%
  .item-info
    padding: .1rem
    .item-title
      line-height: .54rem
      font-size: .32rem
      ellipisis()
    .item-desc
      line-height: .4rem
      color: #ccc
      ellipisis()
</style>
