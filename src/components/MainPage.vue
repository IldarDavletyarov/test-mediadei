<template lang="pug">
.main-page
  builder(:content="content")
</template>
<script>
import BannerBlock from './banner-block.vue';
import WatchNowBlock from './watch-now-block.vue';
import ContinueBlock from './continue-block.vue';
import CardBlock from './card-block.vue';

import Builder from './builder.vue';

export default {
  name: 'MainPage',
  components: {
    BannerBlock,
    WatchNowBlock,
    ContinueBlock,
    CardBlock,
    Builder,
  },
  props: {
    msg: String
  },
  setup() {
    return {
      content: [
        {
          type: 'BannerBlock',
          content: [
            {
              title: 'Dyadya Misha',
              subtitle: 'The clumpsy fellow dispatched to the forest.',
              link: '#',
              image: 'https://s4.vcdn.biz/static/f/769663291/image.jpg',
            },
            {
              title: 'Dyadya Misha',
              subtitle: 'The clumpsy fellow dispatched to the forest.',
              link: '#',
              image: 'https://lh3.googleusercontent.com/proxy/g65z9q-EorKtvVck2UFfm6oLInKHNnk0yx3cnGA7TI9Mk-jDpKA7j4XtKEIQM4H1Bze4mrQBkfLmQcay2loMxJFbgKdumzDffK1hOPbi15Zw3NxjFxKAh1Uu',
            },
            {
              title: 'Dyadya Misha',
              subtitle: 'The clumpsy fellow dispatched to the forest.',
              link: '#',
              image: 'https://skazki.land/api/get-resized-image/dyadya-misha-092a2.jpg?width=1024&height=1024&fit=inside&has-enlargement=1&kernel=cubic',
            },
          ]
        },
        {
          type: 'WatchNowBlock',
          content: {
            image: 'https://cs10.pikabu.ru/post_img/2018/06/20/5/1529479341199516054.jpg',
            link: '#',
          },
        },
        {
          type: 'CardBlock',
          content: {
            title: 'Something Another New',
            cards: [
              {
                image: 'https://upload.wikimedia.org/wikipedia/ru/thumb/b/b4/Harry_Potter_and_the_Philosopher%27s_Stone_—_movie.jpg/208px-Harry_Potter_and_the_Philosopher%27s_Stone_—_movie.jpg',
                title: 'Harry Potter 1: spin off',
                link: '#',
              },
              {
                image: 'https://upload.wikimedia.org/wikipedia/ru/thumb/b/b4/Harry_Potter_and_the_Philosopher%27s_Stone_—_movie.jpg/208px-Harry_Potter_and_the_Philosopher%27s_Stone_—_movie.jpg',
                title: 'Harry Potter 2',
                link: '#',
              },
              {
                image: 'https://upload.wikimedia.org/wikipedia/ru/thumb/b/b4/Harry_Potter_and_the_Philosopher%27s_Stone_—_movie.jpg/208px-Harry_Potter_and_the_Philosopher%27s_Stone_—_movie.jpg',
                title: 'Harry Potter 3',
                link: '#',
              },
              {
                image: 'https://upload.wikimedia.org/wikipedia/ru/thumb/b/b4/Harry_Potter_and_the_Philosopher%27s_Stone_—_movie.jpg/208px-Harry_Potter_and_the_Philosopher%27s_Stone_—_movie.jpg',
                title: 'Harry Potter',
                link: '#',
              },
            ],
          },
        },
        {
          type: 'ContinueBlock',
          content: [
            {
              image: 'https://cs10.pikabu.ru/post_img/2018/06/20/5/1529479341199516054.jpg',
              title: 'Alenkiy cvetochek',
              time: 1000 * 60 * 134.25, // need in timestamp
              percentComplete: '30',
              link: '#',
            },
            {
              image: 'https://cs10.pikabu.ru/post_img/2018/06/20/5/1529479341199516054.jpg',
              title: 'Alenkiy cvetochek',
              time: 1000 * 60 * 100.50, // need in timestamp
              percentComplete: '40',
              link: '#',
            },
            {
              image: 'https://cs10.pikabu.ru/post_img/2018/06/20/5/1529479341199516054.jpg',
              title: 'Alenkiy cvetochek',
              time: 1000* 60 * 43 + 54000, // need in timestamp
              percentComplete: '70',
              link: '#',
            },
          ],
        },
        {
          type: 'CardBlock',
          content: {
          title: 'New',
          cards: [
            {
              image: 'https://upload.wikimedia.org/wikipedia/ru/thumb/b/b4/Harry_Potter_and_the_Philosopher%27s_Stone_—_movie.jpg/208px-Harry_Potter_and_the_Philosopher%27s_Stone_—_movie.jpg',
              title: 'Harry Potter',
              link: '#',
            },
            {
              image: 'https://upload.wikimedia.org/wikipedia/ru/thumb/b/b4/Harry_Potter_and_the_Philosopher%27s_Stone_—_movie.jpg/208px-Harry_Potter_and_the_Philosopher%27s_Stone_—_movie.jpg',
              title: 'Harry Potter',
              link: '#',
            },
            {
              image: 'https://upload.wikimedia.org/wikipedia/ru/thumb/b/b4/Harry_Potter_and_the_Philosopher%27s_Stone_—_movie.jpg/208px-Harry_Potter_and_the_Philosopher%27s_Stone_—_movie.jpg',
              title: 'Harry Potter',
              link: '#',
            },
            {
              image: 'https://upload.wikimedia.org/wikipedia/ru/thumb/b/b4/Harry_Potter_and_the_Philosopher%27s_Stone_—_movie.jpg/208px-Harry_Potter_and_the_Philosopher%27s_Stone_—_movie.jpg',
              title: 'Harry Potter',
              link: '#',
            },
          ],
        },
      }],
    };
  },
};
</script>
<style scoped lang="stylus">
.main-page
  background rgb(13, 19, 41)
  overflow-x hidden
</style>
