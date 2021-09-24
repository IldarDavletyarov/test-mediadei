<template lang="pug">
.main-page
  banner-block(:content="bannerContent")
  watch-now-block(:content="watchContent")
  continue-block(:content="continueContent")
  card-block(:content="cardBlock")
</template>
<script>
import BannerBlock from './banner-block.vue';
import WatchNowBlock from './watch-now-block.vue';
import ContinueBlock from './continue-block.vue';
import CardBlock from './card-block.vue';

export default {
  name: 'MainPage',
  components: {
    BannerBlock,
    WatchNowBlock,
    ContinueBlock,
    CardBlock,
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
      ],
      watchContent: {
        image: 'https://cs10.pikabu.ru/post_img/2018/06/20/5/1529479341199516054.jpg',
      },
      continueContent: [
        {
          image: 'https://cs10.pikabu.ru/post_img/2018/06/20/5/1529479341199516054.jpg',
          title: 'Alenkiy cvetochek',
          time: '1:04:23', // need in timestamp
          percentComplete: '30',
        },
        {
          image: 'https://cs10.pikabu.ru/post_img/2018/06/20/5/1529479341199516054.jpg',
          title: 'Alenkiy cvetochek',
          time: '2:04:23', // need in timestamp
          percentComplete: '40',
        },
        {
          image: 'https://cs10.pikabu.ru/post_img/2018/06/20/5/1529479341199516054.jpg',
          title: 'Alenkiy cvetochek',
          time: '3:04:23', // need in timestamp
          percentComplete: '70',
        },
      ],
      cardBlock: {
        type: 'card-block',
        content: {
          title: 'New',
          cards: [
            {
              image: 'https://upload.wikimedia.org/wikipedia/ru/thumb/b/b4/Harry_Potter_and_the_Philosopher%27s_Stone_—_movie.jpg/208px-Harry_Potter_and_the_Philosopher%27s_Stone_—_movie.jpg',
              title: 'Harry Potter',
            },
            {
              image: 'https://upload.wikimedia.org/wikipedia/ru/thumb/b/b4/Harry_Potter_and_the_Philosopher%27s_Stone_—_movie.jpg/208px-Harry_Potter_and_the_Philosopher%27s_Stone_—_movie.jpg',
              title: 'Harry Potter',
            },
            {
              image: 'https://upload.wikimedia.org/wikipedia/ru/thumb/b/b4/Harry_Potter_and_the_Philosopher%27s_Stone_—_movie.jpg/208px-Harry_Potter_and_the_Philosopher%27s_Stone_—_movie.jpg',
              title: 'Harry Potter',
            },
            {
              image: 'https://upload.wikimedia.org/wikipedia/ru/thumb/b/b4/Harry_Potter_and_the_Philosopher%27s_Stone_—_movie.jpg/208px-Harry_Potter_and_the_Philosopher%27s_Stone_—_movie.jpg',
              title: 'Harry Potter',
            },
          ],
        },
      },
    };
  },
};
</script>
<style scoped lang="stylus">
.main-page
  background rgb(13, 19, 41)
</style>
