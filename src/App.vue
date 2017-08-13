<template lang="pug">
  #app
    el-menu(:default-active='activeIndex', mode='horizontal' theme="dark")
      el-menu-item(index='1') First Item
      el-submenu(index='2')
        span(slot='title') Second Item
        el-menu-item(index='2-1') item one
        el-menu-item(index='2-2') item two
        el-menu-item(index='2-3') item three
    svg-logo
    router-view
</template>

<script>
import svgLogo from '@/components/Logo'
export default {
  name: 'app',
  data() {
      return {
        activeIndex: '1',
        activeIndex2: '1'
      };
    },
  components: {
    svgLogo
  }
}
</script>

<style lang="stylus">
@import 'style/main.styl'

.el-menu
  z-index 10
</style>

