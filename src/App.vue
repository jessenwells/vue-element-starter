<template lang="pug">
  #app
    vue-logo
    h1 {{ msg }}
    el-button(@click.native="startHacking" type="primary" size="large") Yes!
    router-view
</template>

<script>

import vueLogo from '@/components/Logo'
export default {
  name: 'app',
  data () {
    return {
      msg: 'Want something new?'
    }
  },
  methods: {
    startHacking () {
      this.$notify({
        title: 'Vue JS + Element UI',
        message: 'Progressive JavaScript Framework and Component Library for developers',
        duration: 6000
      })
    }
  },
  components: {
    vueLogo
  }
}
</script>

<style lang="stylus">
@import 'style/main.styl'
</style>

