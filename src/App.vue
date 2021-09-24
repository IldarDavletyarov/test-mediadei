<template lang="pug">
main
  header
    .wrapper
      .logo B
      .links
        a(v-for="link in links" :key="link.link" :href="link.link") {{ link.title }}
      div
  main-page
</template>

<script>
import MainPage from './components/MainPage.vue';

const links = [
  {
    title: 'Shorts',
    link: '#',
  },
  {
    title: 'Movies',
    link: '#',
  },
  {
    title: 'Series',
    link: '#',
  },
];

export default {
  name: 'App',
  components: {
    MainPage
  },
  setup() {
    return {
      links,
    };
  },
};
</script>
<style lang="stylus">
html
  body
    margin 0 !important
    padding 0 !important
#app
  font-family Avenir, Helvetica, Arial, sans-serif
  -webkit-font-smoothing antialiased
  -moz-osx-font-smoothing grayscale
  main
    position relative
    header
      position absolute
      top 0
      left 0
      right 0
      z-index 1
      box-shadow: 0px 100px 27px -63px rgba(0, 0, 0, 0.92) inset;
      .wrapper
        padding 4px 16px 12px
        display flex
        align-items center
        justify-content space-between
        color #fff
        .logo
          font-size 36px
          font-weight 600
          font-style italic
        .links
          display flex
          a
            text-decoration none
            color #fff !important
            font-weight 500
            &:not(:last-child)
              margin-right 16px
</style>
