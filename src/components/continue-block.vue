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
      margin-bottom 8px
      .title
        font-size 24px
        font-weight 600
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
        scrollbar-width none
        &::-webkit-scrollbar
          display none
</style>