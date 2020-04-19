<template lang="pug">
.container
  .area
    .firstvue
      .firsttext
        p Akito × Mayu
      .secondtext
        p 兵庫
    .secondvue#trigger
      img#image1(src="~assets/images/index/lgarea/lgthird/1.JPG")
      img#image2(src="~assets/images/index/lgarea/lgthird/2.JPG")
      img#image3(src="~assets/images/index/lgarea/lgthird/3.JPG")
      img#image4(src="~assets/images/index/lgarea/lgthird/4.JPG")
      img#image5(src="~assets/images/index/lgarea/lgthird/5.JPG")
    .thirdvue
      a(href="https://lovegraph.me/albums/18924")
        |view more
</template>

<script>
export default {
  fetch ({store}) {
    store.commit('resetMenu')
  },
  mounted() {
    const scene1 = this.$scrollmagic
      .scene({
        triggerElement: '#trigger',
        triggerHook: 0,
        duration: 300,
        reverse: false
      })
      .setTween('#image1', {
        css: {
          opacity: '1'
        },
      })
    this.$scrollmagic.addScene(scene1)
    const scene2 = this.$scrollmagic
      .scene({
        triggerElement: '#image1',
        triggerHook: 0,
        duration: 300,
        reverse: false
      })
      .setTween('#image2', {
        css: {
          opacity: '1'
        },
      })
    this.$scrollmagic.addScene(scene2)
    const scene3 = this.$scrollmagic
      .scene({
        triggerElement: '#image2',
        triggerHook: 0,
        duration: 300,
        reverse: false
      })
      .setTween('#image3', {
        css: {
          opacity: '1'
        },
      })
    this.$scrollmagic.addScene(scene3)
    const scene4 = this.$scrollmagic
      .scene({
        triggerElement: '#image3',
        triggerHook: 0.5,
        duration: 300,
        reverse: false
      })
      .setTween('#image4', {
        css: {
          opacity: '1'
        },
      })
    this.$scrollmagic.addScene(scene4)
    const scene5 = this.$scrollmagic
      .scene({
        triggerElement: '#image4',
        triggerHook: 0.5,
        duration: 300,
        reverse: false
      })
      .setTween('#image5', {
        css: {
          opacity: '1'
        },
      })
    this.$scrollmagic.addScene(scene5)
  },
}
</script>

<style scoped lang="stylus">
.area
  .firsttext p
    position relative
    display flex
    justify-content center
  .secondtext
    width 100%
    height 10vh
    position relative
    p
      position relative
      height 100vh
      display flex
      justify-content center
  .secondvue
    img
      opacity 0
      width 100vw
      overflow hidden
  .thirdvue
    a
      text-decoration none
      position relative
      display flex
      justify-content center
      color black
</style>