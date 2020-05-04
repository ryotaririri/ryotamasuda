<template lang="pug">
.navbar.is-white
  .navbar-brand
    .navbar-item
    .navbar-burger(data-target="navMenu", v-on:click="$store.commit('toggleMenu')", v-bind:class="{'is-active': $store.state.isMenuActive}") 
      span.span1
      span.span2
      span.span3
  .navbar-menu#navMenu(v-bind:class="{'is-active': $store.state.isMenuActive}")
    .nav-wrap
      .nav-bg
      ul.gnav
        li
          nuxt-link(to="/")
            |Home
        li
          nuxt-link(to="/lg-gallery")
            |Lovegraph gallery
        li
          nuxt-link(to="/private-gallery")
            |Private gallery
        li
          nuxt-link(to="/preset")
            |Preset
        li
          nuxt-link(to="/about")
            |About
</template>

<style scoped lang="stylus">
.navbar-brand
  position relative
  top 12px

span
  position fixed
  right 30px
  width 24px
  height 1px
  background-color #111
  transition all .6s
  z-index 9999

.span1
  top 30px
.span2
  top 38px
.span3
  top 46px

.is-active .span1
  transform rotate(-45deg)
  top 38px
  background-color white
.is-active .span2
  width 0
  left 100%
.is-active .span3
  transform rotate(45deg)
  top 38px
  background-color white

.nav-wrap
  position fixed
  opacity 0
  width 100vw
  height 100vh
  transition all .6s
  line-height 5

.is-active .nav-wrap
  opacity 1
  z-index 999

ul.gnav
  list-style none
  position relative
  margin 20%
  padding 0
  z-index 700
  li
    text-align center
    position relative
    z-index 1000
    a
      text-decoration none
      color white
      position relative
      z-index 1200

.nav-bg
  position absolute
  left 0
  top 0
  width 100vw
  height 100vh
  transition all .6s
  z-index 0

.is-active .nav-bg
  background-color rgba(0,0,0,0.85)
  position absolute
  z-index 600

</style>