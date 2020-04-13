<template lang="pug">
  .container
    .firstvue
      img(src="~assets/images/index/indextop.JPG")
    .secondvue
      .twitter
        a(href="https://twitter.com/ririri_photo")
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
  }
}
</script>

<style scoped lang="stylus">
.firstvue img
  width 100vw
  height 100vh
  overflow hidden

.twitter
.instagram
.lovegraph
  width 100%
  height 10vh
  position relative
  
  img
    width 7vw
a
  display flex
  justify-content center
</style>
