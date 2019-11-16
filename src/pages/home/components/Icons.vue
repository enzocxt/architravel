<template>
  <div class="icons">
    <swiper>
      <swiper-slide v-for="(page, index) of pages" :key="index">
        <div class="icon" v-for="icon of page" :key="icon.id">
          <div class="icon-img">
            <img class="icon-img-content" :src="icon.imgUrl" />
          </div>
          <p class="icon-desc">{{ icon.desc }}</p>
        </div>
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  data () {
    return {
      iconList: [
        {
          id: '0001',
          imgUrl: 'http://www.thearchitecturemaps.com/images/app%20icon%20800x800px.jpg',
          desc: 'city'
        }, {
          id: '0002',
          imgUrl: 'http://www.thearchitecturemaps.com/images/app%20icon%20800x800px.jpg',
          desc: 'country'
        }, {
          id: '0003',
          imgUrl: 'http://www.thearchitecturemaps.com/images/app%20icon%20800x800px.jpg',
          desc: 'country'
        }, {
          id: '0004',
          imgUrl: 'http://www.thearchitecturemaps.com/images/app%20icon%20800x800px.jpg',
          desc: 'country'
        }, {
          id: '0005',
          imgUrl: 'http://www.thearchitecturemaps.com/images/app%20icon%20800x800px.jpg',
          desc: 'country'
        }, {
          id: '0006',
          imgUrl: 'http://www.thearchitecturemaps.com/images/app%20icon%20800x800px.jpg',
          desc: 'country'
        }, {
          id: '0007',
          imgUrl: 'http://www.thearchitecturemaps.com/images/app%20icon%20800x800px.jpg',
          desc: 'country'
        }, {
          id: '0008',
          imgUrl: 'http://www.thearchitecturemaps.com/images/app%20icon%20800x800px.jpg',
          desc: 'country'
        }, {
          id: '0009',
          imgUrl: 'http://www.thearchitecturemaps.com/images/app%20icon%20800x800px.jpg',
          desc: 'country'
        }, {
          id: '0010',
          imgUrl: 'http://www.thearchitecturemaps.com/images/app%20icon%20800x800px.jpg',
          desc: 'country'
        }
      ]
    }
  },
  computed: {
    pages () {
      const pages = []
      this.iconList.forEach((icon, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(icon)
      })
      return pages
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~@styles/variables.styl'
  @import '~@styles/mixins.styl'
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
