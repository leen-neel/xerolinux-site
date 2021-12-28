<template>
  <q-page>
    <Hero />

    <AnnouncementBanner :hasAnnoouncement="true">
      New: XFCE Edition is Live!!!

      <template v-slot:badge> Announcement </template>
    </AnnouncementBanner>

    <About />

    <q-card
      class="
        bg-secondary
        text-white
        q-ma-md
        flex flex-center
        text-h4
        q-pa-lg
        radius-16
      "
    >
      New to Linux?
      <a
        class="q-ml-sm"
        href="https://www.youtube.com/watch?v=tDRjxcCKksU"
        target="_blank"
        >Click me</a
      >
    </q-card>

    <Editions />

    <XeroPorn />

    <Gallery />
  </q-page>
</template>

<script>
import About from "src/components/sections/About.vue";
import Editions from "src/components/sections/Editions.vue";
import Gallery from "src/components/sections/Gallery.vue";
import Hero from "src/components/sections/Hero.vue";
import AnnouncementBanner from "src/components/sections/AnnouncementBanner.vue";
import XeroPorn from "src/components/sections/XeroPorn.vue";

import { defineComponent } from "vue";

export default defineComponent({
  name: "PageIndex",
  components: {
    About,
    Hero,
    Editions,
    Gallery,
    XeroPorn,
    AnnouncementBanner,
  },
});
</script>
