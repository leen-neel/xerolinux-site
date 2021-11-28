<template>
  <div id="gallery" class="text-h2 q-mt-sm text-center q-pa-sm">Gallery</div>

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
    >
      <q-carousel-slide :name="1" img-src="https://i.imgur.com/HERtYR3.png" />
      <q-carousel-slide :name="2" img-src="https://i.imgur.com/znyvRo5.jpg" />
      <q-carousel-slide :name="3" img-src="https://i.imgur.com/rrPrP1d.jpg" />
    </q-carousel>
  </q-responsive>
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
