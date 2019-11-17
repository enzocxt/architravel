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
  </div>
</template>

<script>
export default {
  name: 'HomeHeader'
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
</style>
