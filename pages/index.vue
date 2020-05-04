<template lang="pug">
  .container
    .firstvue
      img(src="~assets/images/index/indextop.JPG")
      p Ryota Masuda
    .link-icon
      .twitter
        a(href="https://twitter.com/ryota__masuda")
          img(src="~assets/images/index/twitter.png")
          p Twitter
      .instagram
        a(href="https://www.instagram.com/ririri.photograph")
          img(src="~assets/images/index/instagram.png")
          p instagram
      .lovegraph
        a(href="https://lovegraph.me/photographers/ri-ri-ri")
          img(src="~assets/images/index/lovegraph.png")
          p lovegraph
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  },
  fetch ({store}) {
    store.commit('resetMenu')
  },
}
</script>

<style scoped lang="stylus">
.firstvue img
  width 100vw
  height 100vh
  position relative
  overflow hidden
  z-index 90
  animation fadein 2s ease 0s 1 normal

@keyframes fadein
  0% 
    opacity:0
  100% 
    opacity:1

.firstvue p
  position absolute
  top 50%
  left 50%
  transform translate(-50%,-50%)
  opacity 0
  animation fadein 3s ease 3s 1 normal
  animation-fill-mode forwards
  font-family: Antro;
  font-size 25px
  z-index 95

.twitter
  margin-top 10%
  
.link-icon
  position relative
  z-index 200

  .twitter
  .instagram
  .lovegraph
    height 10vh
    
    img
      width 30px
      height 30px
    p
      margin-top 0.5%
      margin-left 10%
    
  a
    display flex
    justify-content flex-start
    width 25%
    color black
    text-decoration none
    margin 0 auto
</style>
