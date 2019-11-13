<template>
  <div class="header">
    <div class="header-left"></div>
    <div class="header-input"></div>
    <div class="header-right"></div>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader'
}
</script>

<!-- scoped 限制 .header 只对该 component 中有效 -->
<style lang="stylus" scoped>
  .header
    display: flex
    height: .86rem
    .header-left
      width: .64rem
      float: left
    .header-input
      flex: 1
    .header-right
      width: .64rem
      float: right
</style>
