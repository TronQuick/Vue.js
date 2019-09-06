<!--https://imgs.qunarzz.com/vc/fd/55/94/6c7152c2a8b35a9c49bb26ea25.png_92.png-->
<!--https://imgs.qunarzz.com/vc/eb/d9/1b/e24bca3f1ef6ae6ebdee15e4ca.png_92.png-->
<!--https://imgs.qunarzz.com/vc/c8/01/32/8f6e29b7b6ce0a807742c2587a.png_92.png-->
<!--https://imgs.qunarzz.com/vc/c3/f2/54/2e1c8f9403de1ed28895c9ffa4.png_92.png-->
<!--https://imgs.qunarzz.com/vc/68/4a/91/b7f09964d1e7a6280cca361c46.png_92.png-->
<!--https://imgs.qunarzz.com/vc/77/21/6b/64a35f4ab3ab1fad57731edb3d.png_92.png-->
<template>
  <div class="icons">
    <swiper :options="swiperOption">
      <swiper-slide>
        <div
          class="icon"
          v-for="item of iconList"
          :key="item.id"
        >
          <div class='icon-img'>
            <img class='icon-img-content' :src='item.imgUrl' />
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
        imgUrl: 'https://imgs.qunarzz.com/vc/fd/55/94/6c7152c2a8b35a9c49bb26ea25.png_92.png',
        desc: '主题游'
      }, {
        id: '0002',
        imgUrl: 'https://imgs.qunarzz.com/vc/eb/d9/1b/e24bca3f1ef6ae6ebdee15e4ca.png_92.png',
        desc: '徒步登山'
      }, {
        id: '0003',
        imgUrl: 'https://imgs.qunarzz.com/vc/eb/d9/1b/e24bca3f1ef6ae6ebdee15e4ca.png_92.png',
        desc: '深度游'
      }, {
        id: '0004',
        imgUrl: 'https://imgs.qunarzz.com/vc/c3/f2/54/2e1c8f9403de1ed28895c9ffa4.png_92.png',
        desc: '亲子游'
      }, {
        id: '0005',
        imgUrl: 'https://imgs.qunarzz.com/vc/68/4a/91/b7f09964d1e7a6280cca361c46.png_92.png',
        desc: '潜水'
      }, {
        id: '0006',
        imgUrl: 'https://imgs.qunarzz.com/vc/77/21/6b/64a35f4ab3ab1fad57731edb3d.png_92.png',
        desc: '高空玩乐'
      }]
    }
  },
  computed: {
    // eslint-disable-next-line vue/return-in-computed-property
    pages () {
      const pages = []
      this.iconList.forEach((item,index) => {
        const page = M
      })
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~@/assets/styles/varibles.styl'
  @import '~@/assets/styles/mixins.styl'
  .icons >>> .swiper-container
    height: 0
    padding-bottom: 50%

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
        padding: .1rem

        .icon-img-content
          display: block
          margin: 0 auto
          height: 100%

      .icon-desc
        font-family "微软雅黑 Light"
        font-weight bold
        position: absolute
        left: 0
        right: 0
        bottom: 0
        height: .44rem
        line-height: .44rem
        text-align: center
        color: $darkTextColor
        ellipsis()
</style>
