<template lang="pug">
.card-block
  .card-wrapper
    .header
      .title {{ content.content.title }}
    .content
      .card-list
        card(v-for="(card, index) in content.content.cards" :key="index" :card="card")
      
</template>
<script>
import Card from './card.vue';

export default {
  components: {
    Card,
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
.card-block
  .card-wrapper
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
        grid-auto-columns 140px
        grid-auto-flow column
        scrollbar-width none
        &::-webkit-scrollbar
          display none
</style>