<template lang='pug'>
VideoSlide(src='/video/background.mp4') 
  .flex.place-content-center
    VueFlip(
      active-click
      width='383px'
      height='659px'
    )
      template(v-slot:front)
        .w-full.h-full.flex.place-content-center
          img.object-scale-down(:src='src')
      template(v-slot:back)
        .w-full.px-5(
          class="h-4/5 mt-[44px] rounded-[20px]" 
          :style="{ backgroundColor: `#${background}` }"
        )
          slot
</template>

<script>
import { VueFlip } from 'vue-flip'

import Reveal from '@/components/base/Reveal.vue'
import VideoSlide from '@/components/base/VideoSlide.vue'

export default {
  name: 'PokemonCard',
  components: {
    VueFlip,
    VideoSlide
  },
  props: {
    src: String,
    background: { 
      type: String,
      default: '95908a'
    }
  }
}
</script>

<style lang='scss' scoped>
</style>
