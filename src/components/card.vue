<template lang="pug">
.card
  .content
    img(:src="card.image")
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
.card
  border-radius 8px
  width 100%
  .content
    position relative
    img
      width 100%
      border-radius 8px
    .title
      position absolute
      left 0
      bottom 0
      padding 8px
      right 0
      color #fff
      font-weight 600

</style>