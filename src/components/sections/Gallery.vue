<template>
  <div id="gallery" class="text-h2 q-mt-sm text-center q-pa-sm">Gallery</div>

  <div class="q-pa-md">
    <q-responsive :ratio="16 / 9">
      <q-carousel
        swipeable
        animated
        arrows
        autoplay
        class="q-mt-sm"
        v-model="slide"
        transition-prev="rotate"
        transition-next="rotate"
        infinite
        navigation
        style="border-radius: 16px"
      >
        <q-carousel-slide :name="1" img-src="https://i.imgur.com/HERtYR3.png" />
        <q-carousel-slide
          :name="2"
          img-src="https://cdn.discordapp.com/attachments/912888928749645896/917800804096806942/New.jpg"
        />
        <q-carousel-slide :name="3" img-src="https://i.imgur.com/rrPrP1d.jpg" />
        <q-carousel-slide
          :name="4"
          img-src="https://cdn.discordapp.com/attachments/912888928749645896/927539790113566720/shot.png"
        />
        <q-carousel-slide
          :name="5"
          img-src="https://media.discordapp.net/attachments/910111834206511175/925071385951358986/unknown.png"
        />
      </q-carousel>
    </q-responsive>
  </div>
</template>

<script>
import { ref } from "vue";

export default {
  setup() {
    return {
      slide: ref(1),
      fullscreen: ref(false),
    };
  },
};
</script>
