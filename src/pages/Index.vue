<template>
  <q-page>
    <Hero />

    <AnnouncementBanner :hasAnnoouncement="true">
      <template v-slot:badge> Announcement </template>

      <p style="margin: 0">
        BTRFS & Kernel 5.16 Bug Fixed!!
        <a
          href="https://forum.xerolinux.xyz/thread-78.html"
          style="display: inline"
          target="_blank"
        >
          Check it out!
        </a>
      </p>
    </AnnouncementBanner>

    <About />

    <Download />

    <Customization />
  </q-page>
</template>

<script>
import About from "src/components/sections/About.vue";
import Download from "src/components/sections/Download.vue";
import Hero from "src/components/sections/Hero.vue";
import AnnouncementBanner from "src/components/sections/AnnouncementBanner.vue";
import Customization from "src/components/sections/Customization.vue";

import { defineComponent } from "vue";

export default defineComponent({
  name: "PageIndex",
  components: {
    About,
    Hero,
    Download,
    Customization,
    AnnouncementBanner,
  },
});
</script>

<style lang="scss" scoped>
.new-user {
  max-width: 80vw;
  flex-grow: 1;
}
</style>
