<template lang="pug">
  #app
    img(src="./assets/logo.png")
    h1 {{ msg }}
    el-button(@click.native="startHacking") Yes!
</template>

<script>
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
        title: 'Shhh',
        message: 'Just be patient...',
        duration: 6000
      })
    }
  }
}
</script>

<style lang="stylus">
#app
  font-family sans-serif
  text-align center
</style>

