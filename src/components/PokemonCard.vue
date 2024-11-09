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
  a(:href='src')
    button.inline-flex.items-center.gap-x-2.rounded-md.bg-sky-600.text-sm.font-semibold.text-white.shadow-sm(
  class="hover:bg-sky-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-sky-600 px-3.5 py-2.5"
  type="button"
    )
      ArrowDownTrayIcon.h-5.w-5(
        class='ml-0.5'
        aria-hidden="true"
      )
       | Download
</template>

<script>
import { VueFlip } from 'vue-flip'
import { ArrowDownTrayIcon } from '@heroicons/vue/20/solid'

import Reveal from '@/components/base/Reveal.vue'
import VideoSlide from '@/components/base/VideoSlide.vue'

export default {
  name: 'PokemonCard',
  components: {
    VueFlip,
    VideoSlide,
    ArrowDownTrayIcon
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
