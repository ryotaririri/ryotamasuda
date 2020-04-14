<template lang="pug">
.firstvue
  .firsttext
    p Private gallery
  .secondtext
    p Scroll
    .arrow
</template>

<style scoped lang="stylus">
.firsttext
.secondtext
  width 100%
  height 10vh
  position relative

p
  display flex
  justify-content center

.arrow
  position absolute
  top 1.25em
  left 1em
  animation 2s arrow-animation infinite ease-in-out
  width 0
  height 5em
  border .5px solid #F5F5F5
  &::after
    content ''
    display block
    position absolute
    top 100%
    left -2px
    width 1px
    height 10px
    border-top 10px solid #F5F5F5
    border-left 2px solid transparent
    border-right 2px solid transparent

@keyframes arrow-animation 
  0%
    height:1vh
  100% 
    height:5vh
  
</style>




