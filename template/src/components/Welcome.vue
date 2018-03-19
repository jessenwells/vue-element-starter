<template lang="pug">
  div
    h1 {{ msg }}
    el-button(@click.native="startHacking" type="success" size="large") Yes!
    p {{ hello }}
</template>


<script>
export default {
  name: 'hello',
  data () {
    return {
      msg: 'Want something New?',
      hello: 'App Works!'
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
  }
}
</script>

<style lang="stylus" scoped>

</style>

