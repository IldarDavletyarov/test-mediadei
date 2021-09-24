<template lang="pug">
.watch-now-block
  .watch-now-wrapper
    .header
      .title Watch now
      .live-status Live
    .content
      img(:src="content.image")
</template>
<script>
export default {
  props: {
    content: {
      type: Object,
      default: () => ({}),
    },
  },
};
</script>
<style lang="stylus" scoped>
.watch-now-block
  .watch-now-wrapper
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
      .live-status
        font-size 12px
        line-height 12px
        border-radius 4px
        background rgba(255,255,255,0.2)
        padding 5px
        position relative
        display flex
        align-items center
        font-weight 600
        &::before
          content ""
          display block
          height 6px
          width 6px
          border-radius 3px
          background-color red
          margin 4px
    .content
      width 100%
      z-index 1
      cursor pointer
      margin-top 8px
      img
        max-width 100%
        border-radius 8px
</style>