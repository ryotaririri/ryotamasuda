<template lang="pug">
.container
  .area
    .firstvue
      .Lovegraph-title
        p Lovegraph gallery
      .Scroll-title
        p Scroll
        .arrow
  .area
    .secondvue
      nuxt-link(to="/lg-first")
        img(src="~assets/images/index/lgarea/lgfirst/firsttop.JPG")
  .area
    .secondvue
      nuxt-link(to="/lg-second")
        img(src="~assets/images/index/lgarea/lgsecond/secondtop.JPG")
  .area
    .secondvue
      nuxt-link(to="/lg-third")
        img(src="~assets/images/index/lgarea/lgthird/thirdtop.JPG")
  .area
    .secondvue
      nuxt-link(to="/lg-fourth")
        img(src="~assets/images/index/lgarea/lgfourth/fourthtop.JPG") 
  .area
    .secondvue
      nuxt-link(to="/lg-fifth")
        img(src="~assets/images/index/lgarea/lgfifth/fifthtop.JPG")
      
</template>

<script>
export default {
  fetch ({store}) {
    store.commit('resetMenu')
  }
}
</script>

<style scoped lang="stylus">
.container
  position relative
  scroll-snap-type mandatory
  scroll-snap-points-y repeat(100vh)
  scroll-snap-type y mandatory
  height 100vh
  width 100%
  -webkit-overflow-scrolling touch
  overflow-scrolling touch
  overflow-y scroll
  overflow-x hidden
  text-align center

  .area
    position relative
    height 100%
    width 100%
    scroll-snap-align start
    text-align center
    .Lovegraph-title p
      position absolute
      top 40%
      font-size 1.2rem
      letter-spacing 3px
      padding 5px 10px
      left 50%
      transform translate(-50%,-50%)
      border-top 1px solid #283246
      border-bottom 1px solid #283246

    .Scroll-title
      width 100%
      height 50vh
      position relative
      p
        position relative
        top 100%
        height 100vh
        display flex
        justify-content center

    .arrow
      position absolute
      top 30em
      left 11.5em
      animation 2s arrow-animation infinite ease-in-out
      width 0
      height 5em
      border .5px solid #000
      &::after
        content ''
        display block
        position absolute
        top 100%
        left -2px
        width 1px
        height 10px
        border-top 10px solid #000
        border-left 2px solid transparent
        border-right 2px solid transparent
          
    img
      height 100vh
      overflow hidden

@keyframes arrow-animation 
  0%
    height:1vh
  100% 
    height:5vh
</style>