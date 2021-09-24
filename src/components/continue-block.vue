<template lang="pug">
.continue-block
  .continue-wrapper
    .header
      .title Continue watching
    .content
      .card-list
        preview-continue-card(v-for="(card, index) in content" :key="index" :card="card")
      
</template>
<script>
import PreviewContinueCard from './preview-continue-card.vue';

export default {
  components: {
    PreviewContinueCard,
  },
  props: {
    content: {
      type: Object,
      default: () => ({}),
    },
  },
};
</script>
<style lang="stylus" scoped>
.continue-block
  .continue-wrapper
    padding 8px
    color #fff
    .header
      display flex
      justify-content space-between
      align-items center
      .title
        font-size 24px
        font-weight 600
      .live-status
        font-weight 600
        font-size 18px
        line-height 18px
        border-radius 4px
        background rgba(255,255,255,0.4)
        padding 6px
        position relative
        display flex
        align-items center
        &::before
          content ""
          display block
          height 8px
          width 8px
          border-radius 4px
          background-color red
          margin 4px
    .content
      width 100%
      overflow hidden
      .card-list
        overflow-x auto
        display inline-grid
        max-width 100%
        grid-column-gap 8px
        grid-auto-columns 280px
        grid-auto-flow column
</style>