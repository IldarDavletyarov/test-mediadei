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
      .title
        font-size 32px
        font-weight 600
      .live-status
        font-weight 600
        font-size 18px
        line-height 18px
        border-radius 4px
        background rgba(255,255,255,0.4)
        padding 6px
        position relative
        &::after
          content ''
          position relative
          height 4px
          width 4px
          border-radius 4px
          background-color red
    .content
      width 100%
      z-index 1
      img
        max-width 100%
        border-radius 8px
</style>