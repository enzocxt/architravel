<template>
  <div>
    <div class="recommend-title">Recommendations</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <div class="item-img-wrapper">
          <swiper :options="swiperOption">
            <swiper-slide v-for="img of item.imgList" :key="img.imgId">
              <img class="item-img" :src="img.imgUrl" />
            </swiper-slide>
          </swiper>
        </div>
        <p class="item-title">{{ item.title }}</p>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      swiperOption: {
        loop: false
      },
      recommendList: [{
        id: '0001',
        imgList: [{
          imgId: '0001',
          imgUrl: 'https://skogskyrkogarden.stockholm.se/globalassets/2-om-platsen/byggnader/uppstandelsekapellet_1560x484_int.jpg'
        }, {
          imgId: '0002',
          imgUrl: 'https://skogskyrkogarden.stockholm.se/globalassets/2-om-platsen/byggnader/uppstandelse-ny_1650x484_to.jpg?preset=fullbredd-kort-full'
        }, {
          imgId: '0003',
          imgUrl: 'https://skogskyrkogarden.stockholm.se/globalassets/2-om-platsen/byggnader/mosaik_detalj.jpg'
        }],
        title: 'Chapel of Resurrection'
      }, {
        id: '0002',
        imgList: [{
          imgId: '0001',
          imgUrl: 'https://s3.amazonaws.com/gs-geo-images/be5a406d-8ad0-48d0-8057-12a1d5156498.jpg'
        }, {
          imgId: '0002',
          imgUrl: 'https://img1.oastatic.com/img2/18011684/834x417r/sankt-petri-kyrka-i-klippan-taend-ett-ljus.jpg'
        }],
        title: 'Sankt Petri Kyrka'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~@styles/mixins.styl'
  .recommend-title
    margin-top: .2rem
    line-height: .8rem
    background: #eee
    text-indent: .2rem
  .item
    position: relative
    overflow: hidden
    display: flex
    .item-img-wrapper
      /* position: relative */
      overflow: hidden
      width: 100%
      height: 0
      padding-bottom: 35%
      .item-img
        width: 100%
    .item-title
      position: absolute
      line-height: .54rem
      font-size: .32rem
      bottom: .18rem
      margin-left: .2rem
      color: #fff
      z-index: 1
      ellipsis()
</style>
