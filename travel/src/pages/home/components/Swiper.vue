<template>
  <div class="wrapper">
    <swiper :options="swiperOption" >
      <!-- slides -->
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl"/>
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
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
        loop: true,
        autoplay: true,
        speed: 4000
      },
      swiperList: [{
        id: '0001',
        imgUrl: 'https://source.qunarzz.com/site/images/wns/20190903_qunar_dujia_750x192_6_V1.jpg'
      }, {
        id: '0002',
        imgUrl: 'https://source.qunarzz.com/site/images/wns/20190819_750x192_11685.jpg'
      }, {
        id: '0003',
        imgUrl: 'https://source.qunarzz.com/site/images/wns/20190815_750x192_11527.jpg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background: #fff !important
  .wrapper
    overflow: hidden
    width: 100%
    height: 0
    padding-bottom: 25.59%
    .swiper-img
      width: 100%
</style>
