<template>
  <div id="app">
    <keep-alive>
    <!-- <keep-alive exclude="detail"> -->
      <router-view/>
    </keep-alive>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style></style>
