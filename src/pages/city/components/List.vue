<template>
  <div class="list" ref="wrapper">
    <div>
      <div class="area">
        <div class="title border-topbottom">Current City</div>
        <div class="button-list">
          <div class="button-wrapper">
            <div class="button">Paris</div>
          </div>
        </div>
      </div>
      <div class="area">
        <div class="title border-topbottom">Popular Cities</div>
        <div class="button-list">
          <div class="button-wrapper">
            <div class="button">Paris</div>
          </div>
          <div class="button-wrapper">
            <div class="button">Barcelona</div>
          </div>
          <div class="button-wrapper">
            <div class="button">London</div>
          </div>
          <div class="button-wrapper">
            <div class="button">Stockholm</div>
          </div>
          <div class="button-wrapper">
            <div class="button">Tokyo</div>
          </div>
        </div>
      </div>
      <div class="area">
        <div class="title border-topbottom">A</div>
        <div class="button-list">
          <div class="button-wrapper">
            <div class="button">Paris</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Bscroll from 'better-scroll'
export default {
  name: 'CityList',
  mounted () {
    this.scroll = new Bscroll(this.$ref.wrapper)
  }
}
</script>

<style lang="stylus" scoped>
  @import '~@styles/variables.styl'
  .border-topbottom
    &:before
      border-color: #ccc
    &:after
      border-color: #ccc

  .list
    overflow: hidden
    position: absolute
    top: 1.58rem
    left: 0
    right: 0
    bottom: 0
    .title
      line-height: .54rem
      padding-left: .2rem
      background: #eee
      color: #666
      font-size: .26rem
    .button-list
      overflow: hidden
      padding: .1rem .6rem .1rem .1rem
      .button-wrapper
        float: left
        width: 33.33%
        .button
          margin: .1rem
          padding: .1rem 0
          text-align: center
          border: .02rem solid #ccc
          border-radius: .06rem
</style>
