<template lang="pug">
.builder
  component(v-for="(block, index) in blocks" :key="index" :is="block.component" :content="block.content") 
</template>
<script>
import { computed } from 'vue';
import BannerBlock from './banner-block.vue';
import WatchNowBlock from './watch-now-block.vue';
import ContinueBlock from './continue-block.vue';
import CardBlock from './card-block.vue';

const contentMapper = {
  'CardBlock': CardBlock,
  'BannerBlock': BannerBlock,
  'WatchNowBlock': WatchNowBlock,
  'ContinueBlock': ContinueBlock,
};

export default {
  props: {
    content: {
      type: Array,
      default: [],
    },
  },
  setup(props) {
    const blocks = computed(() => props.content.map(_ => ({ component: contentMapper[_.type], content: _.content })));
    return {
      blocks,
    };
  },
};
</script>