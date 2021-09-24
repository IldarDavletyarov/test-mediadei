<template lang="pug">
.preview-continue-card
  .content
    img(:src="card.image")
    .status
      .time {{ new Date(card.time).toISOString().substr(11, 8) }}
      .status-line
        .line-complete(:style="{ '--percentage': card.percentComplete }")
  .title {{ card.title }}
  
</template>
<script>
export default {
  props: {
    card: {
      type: Object,
      default: () => ({}),
    },
  },
};
</script>
<style lang="stylus" scoped>
.preview-continue-card
  border-radius 8px
  width 100%
  .content
    position relative
    overflow hidden
    img
      width 100%
      border-radius 8px
    .status
      position absolute
      left 0
      bottom 0
      padding 8px
      right 0
      box-shadow 0px -38px 23px -25px rgba(0, 0, 0, 1) inset;
      border-radius 8px
      .time
        margin-left auto
        font-size 8px
        text-align right
        color rgba(255,255,255,0.96)
        margin-bottom 4px
      .status-line
        width 100%
        height 4px
        border-radius 2px
        background rgba(255,255,255,0.4)
        .line-complete
          --percentage 50%
          width calc(1% * var(--percentage))
          border-radius 2px
          height 2px
          background rgb(103, 131, 221)
  .title
    margin-top 8px
    font-weight 600

</style>