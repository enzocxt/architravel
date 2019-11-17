<template>
  <div class="header">
    <router-link to="/city">
      <div class="header-left" to="#/city">
        <div class="iconfont menu-icon">&#xe6ec;</div>
      </div>
    </router-link>
    <div class="header-input">
      <div class="iconfont search-icon">&#xe70a;</div>
    </div>
    <router-link to="/city">
      <div class="header-right">
        {{ this.city }}
        <span class="iconfont arrow-icon">&#xe6eb;</span>
      </div>
    </router-link>
  </div>
</template>

<script>
import { mapState } from 'vuex'
export default {
  name: 'HomeHeader',
  computed: {
    ...mapState(['city'])
  }
}
</script>

<style lang="stylus" scoped>
  /* 样式中引入需要用 ~@import */
  @import '~@styles/variables.styl'
  /* 1rem = html font-size = 50px */
  .header
    display: flex
    line-height: .86rem
    background: $bgColor /* #00bcd4 */
    color: #fff
    .header-left
      width: .64rem
      float: left
      color: #fff
      .menu-icon
        text-align: center
        font-size: .4rem
    .header-input
      flex: 1
      height: .64rem
      line-height: .64rem
      margin-top: .12rem
      margin-left: .2rem
      margin-bottom: .12rem
      margin-right: .2rem
      background: #fff
      border-radius: .1rem
      color: #ccc
      .search-icon
        padding-right: .4rem
        float: right
    .header-right
      min-width: 1.04rem
      padding: 0 .1rem
      float: right
      text-align: center
      color: #fff
      .arrow-icon
        margin-left: -.04rem
        font-size: .24rem
</style>
