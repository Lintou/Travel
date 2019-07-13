<template>
  <div class='icons'>
    <swiper>
      <swiper-slide v-for='(page, index) of pages' :key='index'>
        <div class='icon'
             v-for="item of page"
             :key="item.id"
        >
          <div class='icon-img'>
            <img class='icon-img-content' :src='item.imgUrl'>
          </div>
          <p class="icon-desc">{{item.desc}}</p>
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
        imgUrl: '//s.qunarzz.com/vacation_react/around/entry2_2.png',
        desc: '222日游一日游一日游'
      }, {
        id: '0002',
        imgUrl: '//s.qunarzz.com/vacation_react/around/entry3.png',
        desc: '自驾游'
      }, {
        id: '0003',
        imgUrl: '//s.qunarzz.com/vacation_react/around/entry5.png',
        desc: '跟团游'
      }, {
        id: '0004',
        imgUrl: '//s.qunarzz.com/vacation_react/around/entry4.png',
        desc: '景点门票'
      }, {
        id: '0005',
        imgUrl: '//s.qunarzz.com/vacation_react/around/entry1.png',
        desc: '景+酒'
      }, {
        id: '0006',
        imgUrl: '//s.qunarzz.com/vacation_react/around/entry5.png',
        desc: '跟团游'
      }, {
        id: '0007',
        imgUrl: '//s.qunarzz.com/vacation_react/around/entry5.png',
        desc: '跟团游'
      }, {
        id: '0008',
        imgUrl: '//s.qunarzz.com/vacation_react/around/entry5.png',
        desc: '跟团游'
      }, {
        id: '0009',
        imgUrl: '//s.qunarzz.com/vacation_react/around/entry5.png',
        desc: '跟团游'
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
  @import '~styles/varibles.styl';
  @import '~styles/mixins.styl';
  .icons >>> .swiper-container
    height: 0
    padding-bottom: 50%
    // width: 100%
    // overflow: hidden
    // height: 0
    // padding-bottom: 50%
    .icons
      margin-top: .1rem
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
        bottom: .44rem
        box-sizing: border-box
        pading: .1rem
        .icon-img-content
          height: 100%
          display: block
          margin: 0 auto
      .icon-desc
        position: absolute
        left: 0
        right: 0
        bottom: 0
        height: .44rem
        line-height: .44rem
        color: $darkTextColor
        text-align: center
        ellipisis()
</style>
