<template lang="pug">
.banner-block
  carousel
    slide(v-for="(banner, index) in content" :key="index")
      .wrapper
        img(:src="banner.image")
        .actions
          .title {{ banner.title }}
          .subtitle {{ banner.subtitle }}
          .button Play
</template>
<script>
import 'vue3-carousel/dist/carousel.css';
import { Carousel, Slide } from 'vue3-carousel';

export default {
  components: {
    Carousel,
    Slide,
  },
  props: {
    content: {
      type: Object,
      default: () => ({}),
    },
  },
}
</script>
<style lang="stylus" scoped>
.banner-block
  .wrapper
    position relative
    width 100vw
    height 70vh
    img
      width 100%
    .actions
      position absolute
      bottom 0
      left 0
      right 0
      z-index 1
      color #fff
      text-align left
      padding 16px
      box-shadow: 0px -100px 100px -81px rgba(0, 0, 0, 0.92) inset;
      .title
        font-weight 600
        font-size 32px
      .sibtitle
        font-size 18px
        margin-top 8px
      .button
        margin-top 8px
        height 48px
        width min-content
        padding 16px 36px
        border-radius 24px
        background blue
        font-weight 600
        font-size 18px
        transition all .2s ease
        line-height 18px
        cursor pointer
        background rgb(103, 131, 221)
        text-align center
        &:hover
          font-size 19px
          letter-spacing 0px
        
</style>