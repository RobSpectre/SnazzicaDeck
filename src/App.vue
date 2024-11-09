<template lang='pug'>
Reveal
  .slides
    PokemonCard(src='/images/schmerr_card.png' background='ffe557')
      .title.text-outline Snazzisms
      p.copy.text-white
       | This is an example of some text.
    PokemonCard(src='/images/capacious_handpurse.png' background='eae1e0')
      .title.text-outline Ready to Go
      p.copy.text-white
       | Stuff
    PokemonCard(src='/images/putterpoop.png' background='fde16b')
      .title.text-outline Grit
      p.copy.text-white
       | More copy
    PokemonCard(src='/images/popcorn.png' background='da3789')
      .title.text-outline Her Taste
      p.copy.text-white
       | Copy
    PokemonCard(src='/images/steam_roller_card.png')
      .title.text-outline Rolled 
      p.copy.text-white
       | This is
       | A bunch of stuff
       | no linebreaks.
    PokemonCard(src='/images/visor.png' background='305c75')
      .title.text-outline E-Town
      p.copy.text-white
       | Text
    PokemonCard(src='/images/snoozica.png' background='232323')
      .title.text-outline Snooze Abuse
      p.copy.text-white
       | More stuff
    PokemonCard(src='/images/ada.png' background='084182')
      .title.text-outline The Meeting
      p.copy.text-white
       | Copy
    PokemonCard(src='/images/two_of_cups.png' background='393738')
      .title.text-outline First Kiss
      p.copy.text-white
       | Text
</template>

<script>
import Reveal from '@/components/base/Reveal.vue'
import Slide from '@/components/base/Slide.vue'
import VideoSlide from '@/components/base/VideoSlide.vue'

import PokemonCard from '@/components/PokemonCard.vue'

export default {
  name: 'JessBerfday',
  components: {
    Reveal,
    Slide,
    VideoSlide,
    PokemonCard
  }
}
</script>

<style lang='scss'>
@import url('https://fonts.cdnfonts.com/css/pokemon-solid');
@import url('https://fonts.googleapis.com/css2?family=Noto+Sans:ital,wght@0,100..900;1,100..900&display=swap');

.text-outline {
  text-shadow:
    8px 8px 0 #3c61a3,
    -8px 8px 0 #3c61a3,
    8px -8px 0 #3c61a3,
    -8px -8px 0 #3c61a3;
}

.title {
    font-family: 'Pokemon Solid', sans-serif;
    @apply text-7xl pt-12 mx-auto uppercase text-pokemonYellow;
}

.copy {
  font-family: 'Noto Sans', sans-serif;
  @apply text-2xl px-4 py-4 text-left;
}
</style>
