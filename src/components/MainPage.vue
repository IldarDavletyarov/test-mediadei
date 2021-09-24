<template lang="pug">
.main-page
  banner-block(:content="bannerContent")
</template>
<script>
import BannerBlock from './banner-block.vue';

export default {
  name: 'MainPage',
  components: {
    BannerBlock,
  },
  props: {
    msg: String
  },
  setup() {
    return {
      bannerContent: [
        {
          title: 'Dyadya Misha',
          subtitle: 'The clumpsy fellow dispatched to the forest.',
          image: 'https://s4.vcdn.biz/static/f/769663291/image.jpg',
        },
        {
          title: 'Dyadya Misha',
          subtitle: 'The clumpsy fellow dispatched to the forest.',
          image: 'https://lh3.googleusercontent.com/proxy/g65z9q-EorKtvVck2UFfm6oLInKHNnk0yx3cnGA7TI9Mk-jDpKA7j4XtKEIQM4H1Bze4mrQBkfLmQcay2loMxJFbgKdumzDffK1hOPbi15Zw3NxjFxKAh1Uu',
        },
        {
          title: 'Dyadya Misha',
          subtitle: 'The clumpsy fellow dispatched to the forest.',
          image: 'https://skazki.land/api/get-resized-image/dyadya-misha-092a2.jpg?width=1024&height=1024&fit=inside&has-enlargement=1&kernel=cubic',
        },
      ]
    }
  }
}
</script>
<style scoped lang="stylus">
h3
  margin 40px 0 0

ul
  list-style-type none
  padding 0

li
  display inline-block
  margin 0 10px

a
  color #42b983
</style>
