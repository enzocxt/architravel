<template>
  <div>
    <div class="recommend-title">Recommendations</div>
    <ul>
      <router-link tag="li"
        class="item border-bottom"
        v-for="item of list"
        :key="item.id"
        :to="'/detail/' + item.id"
      >
        <div class="item-img-wrapper">
          <swiper :options="swiperOption">
            <swiper-slide v-for="img of item.imgList" :key="img.imgId">
              <img class="item-img" :src="img.imgUrl" />
            </swiper-slide>
          </swiper>
        </div>
        <p class="item-title">{{ item.title }}</p>
      </router-link>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  props: {
    list: Array
  },
  data () {
    return {
      swiperOption: {
        loop: false
      }
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
