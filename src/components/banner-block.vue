<template lang="pug">
.banner-block
  carousel(:autoplay="2000" :items-to-show="1")
    slide(v-for="(banner, index) in content" :key="index")
      .wrapper
        img(:src="banner.image")
        .actions
          .title {{ banner.title }}
          .subtitle {{ banner.subtitle }}
          .button Play
    template(#addons="{ currentSlide }")
      .t {{ currentSlide }}
      pagination(:class="{'init': currentSlide <= -1}")
</template>
<script>
import 'vue3-carousel/dist/carousel.css';
import { Carousel, Slide, Navigation, Pagination} from 'vue3-carousel';

export default {
  components: {
    Carousel,
    Slide,
    Navigation,
    Pagination,
  },
  props: {
    content: {
      type: Object,
      default: () => ({}),
    },
  },
}
</script>
<style lang="stylus">
.banner-block
  .carousel__pagination
    width 100%
    justify-content space-between
    margin 0 !important
    padding 0 8px !important
    position relative
    top -24px
    &.init > li.carousel__pagination-item:first-child > button.carousel__pagination-button
      background rgb(103, 131, 221)
      width calc(50vw - 8px)
    > li.carousel__pagination-item
      width 100%
      > button.carousel__pagination-button
        background grey
        height 3px
        border-radius 1.5px
        width calc(100% - 8px)
        transition background .1s ease
        &.carousel__pagination-button--active
          background rgb(103, 131, 221)
          width calc(50vw - 8px)

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
      box-shadow: 0px -100px 56px -29px rgba(13, 19, 41, 1) inset;
      .title
        font-weight 600
        font-size 24px
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