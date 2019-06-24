<template>
  <div class='wrapper'>
    <swiper :options="swiperOption">
        <!-- slides -->
        <swiper-slide v-for='item of swiperList' :key='item.id'>
        <img class='swiper-img' :src='item.imgUrl'/>
        </swiper-slide>
        <!-- Optional controls -->
        <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>
<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: '0001',
        imgUrl:'https://hbimg.huabanimg.com/f83c242c6987e11073ca9badeb3cfcba3b3a4487297ddf-PIwfmx_fw658'
      },
      {
        id: '0002',
        imgUrl: 'https://hbimg.huabanimg.com/b389355be29da3836d2fc29493be3f8da657a9f59fc1a-WcJ4gg_fw658'
      }]
    }
  }
}
</script>
<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background: #ffffff
  .wrapper
    overflow: hidden
    width: 100%
    height: 0
    padding-bottom: 31.25%  
    background: #eee
    .swiper-img
      width: 100%
</style>
