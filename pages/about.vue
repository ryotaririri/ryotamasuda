<template lang="pug">
.container
  .area
    .firstvue
      .firsttext
        p.subfont About
    .secondvue
      img(src="~assets/images/index/about/about.JPG")
    .thirdvue
      p
        |Ryota Masuda
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
    .Performance-title
      p.subfont Performance
    .Performance-list
      ul.Performance-list
        li
          |2020.2　アカデミー講師賞
        li
          |2020.2　PV賞
        li
          |2019.8　月間作品 優秀賞
        li
          |2019.3　月間作品 優秀賞
        li
          |2019.2　Best Fun賞
        li
          |Platinumラブグラファー(社内上位10％)
        li
          |LGC(ラブグラファー養成講座) チーフトレーナー
        li
          |関西エリアマネージャー
        li
          |ラブグラフアカデミー講師
    .skill-tittle
      p.subfont Skill
    .skill-list
      ul.skill-list
        li
          |写真撮影・編集
        li
          |動画撮影・編集
        li
          |Web開発
          ul.inner-list
            li
              |HTML.CSS
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
export default {
  fetch ({store}) {
    store.commit('resetMenu')
  }
}
</script>

<style scoped lang="stylus">
.area
  .firstvue
    .firsttext
      position relative
      display flex
      justify-content center
      margin-top 2vh
      font-size 2rem
      animation fadein 2s ease 0s 1 normal
      p.subfont
        font-family: Antro;

    @keyframes fadein
      0% 
        opacity:0
      100% 
        opacity:1

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
    animation fadein 2s ease 0s 1 normal

  @keyframes fadein
    0% 
      opacity:0
    100% 
      opacity:1

  .Performance-title
    margin-top 10%
    width 100%
    font-size 2rem
    text-align center
    animation fadein 2s ease 0s 1 normal
    p.subfont
      font-family: Antro;

  @keyframes fadein
    0% 
      opacity:0
    100% 
      opacity:1

  .Performance-list
    width 80%
    letter-spacing 2px
    font-size .8rem
    padding 0
    margin 5% auto

  ul.Performance-list
    margin 5% auto
    border-top 1px solid #283246
    border-bottom 1px solid #283246
    li
      margin 3% auto
      padding 0 5%
      list-style-type none

  .skill-tittle
    margin-top 10%
    width 100%
    font-size 2rem
    text-align center
    p.subfont
      font-family: Antro;

  .skill-list
    width 80%
    letter-spacing 2px
    font-size .8rem
    padding 0
    margin 5% auto

  ul.skill-list
    margin 5% auto
    border-top 1px solid #283246
    border-bottom 1px solid #283246
    li
      margin 3% auto
      padding 0 5%
      list-style-type none
  
  .twitter
    margin-top 10%

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