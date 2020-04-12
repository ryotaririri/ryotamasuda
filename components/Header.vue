<template lang="pug">
.navbar.is-white
  .navbar-brand
    .navbar-item
    .navbar-burger(data-target="navMenu", v-on:click="toggleMenu", v-bind:class="{'is-active': isMenuActive}") 
      span.span1
      span.span2
      span.span3
  .navbar-menu#navMenu(v-bind:class="{'is-active': isMenuActive}")
    .nav-wrap
      .nav-bg
      ul.gnav
        li
          nuxt-link(to="/")
            |Home
        li
          nuxt-link(to="/lg-gallery")
            |Lg gallery
        li
          nuxt-link(to="/private-gallery")
            |Private gallery
        li
          nuxt-link(to="/preset")
            |Preset
        li
          nuxt-link(to="/about")
            |About
        li
          nuxt-link(to="/contact")
            |Contact
</template>

<script>
export default {
  data: () => {
    return {isMenuActive: false}
  },
  methods: {
    toggleMenu () {
      this.isMenuActive = !this.isMenuActive
    }
  }
}
</script>

<style scoped lang="stylus">
span
  position absolute
  left 11px
  width 18px
  height 1px
  background-color #111
  transition all .6s
  z-index 9999

.span1
  top 14px
.span2
  top 20px
.span3
  top 26px

.is-active .span1
  transform rotate(45deg)
  top 20px
  background-color white
.is-active .span2
  width 0
  left 50%
.is-active .span3
  transform rotate(-45deg)
  top 20px
  background-color white

.nav-wrap
  position fixed
  top -100%
  right 0
  width 100vw
  height 100vh
  transition all .6s

.is-active .nav-wrap
  top 0

ul.gnav
  list-style none
  position relative
  z-index 9999
  li
    margin 5.4%
    a
      text-decoration none
      color white

.nav-bg
  position fixed
  left 0
  top 0
  width 100vw
  height 100vh
  transition all .6s
  z-index 0

.is-active .nav-bg
  background-color rgba(0,0,0,0.85)

</style>
