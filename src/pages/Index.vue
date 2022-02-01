<template>
  <q-page>
    <Hero />

    <AnnouncementBanner :hasAnnoouncement="false">
      <template v-slot:badge> Announcement </template>
    </AnnouncementBanner>

    <About />

    <q-card
      class="bg-secondary text-white q-ma-md flex flex-center text-h5 q-pa-sm radius-16"
    >
      New to Linux?
      <q-btn
        color="white"
        size="1em"
        label="Click me"
        noCaps
        class="q-ml-sm"
        flat
        @click="learn = true"
      />
    </q-card>

    <Download />

    <Customization />
  </q-page>

  <q-dialog class="z-top" v-model="learn" pesistent>
    <q-card>
      <q-bar dark class="text-white">
        <q-space />
        <q-btn dense flat round icon="close" color="white" v-close-popup />
      </q-bar>

      <q-card-section class="flex flex-center full-height">
        <q-video
          src="https://www.youtube.com/embed/tDRjxcCKksU?rel=0"
          :aspect-ratio="16 / 9"
        />
      </q-card-section>
    </q-card>
  </q-dialog>
</template>

<script>
import About from "src/components/sections/About.vue";
import Download from "src/components/sections/Download.vue";
import Hero from "src/components/sections/Hero.vue";
import AnnouncementBanner from "src/components/sections/AnnouncementBanner.vue";
import Customization from "src/components/sections/Customization.vue";

import { defineComponent, ref } from "vue";

export default defineComponent({
  name: "PageIndex",
  components: {
    About,
    Hero,
    Download,
    Customization,
    AnnouncementBanner,
  },
  setup() {
    return {
      learn: ref(false),
    };
  },
});
</script>
