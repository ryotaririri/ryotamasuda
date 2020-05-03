<template lang="pug">
.container
  .area
    .firstvue
      .firsttext
        p About
    .secondvue
      img(src="~assets/images/index/about/about.JPG")
    .thirdvue
      p
        R|yota Masuda
        br
        |増田 椋太
        br
        br
        |Photographer／Lovegraph inc.
        br
        br
        br
        |1992年福岡県生まれ。
        |大学にて宗教学や心理学を専攻後、大阪市内のHP制作会社に勤務。
        |平日はWebディレクターとして企業HPの制作・監修を務めながら、2016年12月、株式会社ラブグラフに関西Lovegrapherとして登録。
        |これまで180組以上のゲストを撮影、今日に至る。
    .fourthtitle
      p 実績



</template>

<script>
export default {
  fetch ({store}) {
    store.commit('resetMenu')
  }
}
</script>

<style scoped lang="stylus">
.area
  .firstvue
    .firsttext p
      position relative
      display flex
      justify-content center
      margin-top 2vh
      font-size 2rem
  .secondvue img
    width 100vw
    vertical-align bottom
    position relative
    overflow hidden
    animation fadein 2s ease 0s 1 normal

  @keyframes fadein
    0% 
      opacity:0
    100% 
      opacity:1
  
  .thirdvue p
    width 90%
    letter-spacing 2px
    margin 5% auto

  .fourthtitle p
    margin-top 10%
    width 100%
    font-size 2rem
    text-align center

</style>