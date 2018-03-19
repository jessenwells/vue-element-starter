<template lang="pug">
-v1 = 'M95.04,0l95.04,168l-190.08,0l95.04,-168Z'
-v2 = 'M95.04,67.95l61.624,100.05l-123.248,0l61.624,-100.05Z'
-v3 = 'M95.04,122.992l27.51,45.968l-55.02,0l27.51,-45.968Z'
#box
    svg#logo(viewBox="0 0 190 170")
        g
            path.v1(d=v1)
            path.v2(d=v2)
            path.v3(d=v3)
</template>

<script>
export default {

}
</script>

<style lang="stylus" scoped>
#box
    width 300px
    height 300px
    margin 0 auto
    z-index 1
    #logo
        position relative
        transform rotate(-180deg)
        width 100%
        animation slide 3.5s forwards cubic-bezier(0.25, -0.1, 0.25, 1.25)
        .v1
            fill #41b883
        .v2
            fill #35495e
        .v3
            fill #ffffff
@keyframes slide
  0%
    top -600px
  65%
    top -600px
  90%
    top 70px
  100%
    top 35px
</style>
