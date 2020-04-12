<template lang="pug">
ul.gnav
  li
    nuxt-link(to="/")
      |Home
  li.hov
    nuxt-link(to="/photo")
      |Photo
    ul.lnav
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

<style scoped lang="stylus">
ul.gnav
  display flex
  list-style none
  justify-content space-between
  li
    margin 5.4%
    a
      text-decoration none
      color black
  li.hov:hover
    ul.lnav li
      height 2rem
      overflow visible 
ul.lnav li
  overflow hidden
  height 0
  transition .5s

</style>
  