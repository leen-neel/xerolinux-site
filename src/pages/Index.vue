<template>
  <q-page>
    <Hero />

    <AnnouncementBanner :hasAnnoouncement="true">
      <template v-slot:badge> Announcement </template>

      <p style="margin: 0">
        XFCE is no longer available
        <q-btn
          color="white"
          size="xl"
          label="Learn more"
          @click="popup = true"
          flat
        />
      </p>
    </AnnouncementBanner>

    <About />
    <Features v-if="false" />

    <Download />

    <Customization />
  </q-page>

  <!-- Note -->
  <q-dialog v-model="popup" class="z-top">
    <q-card class="radius-16" style="width: 85%; max-width: 90vw">
      <q-bar dark class="text-white">
        <q-space />
        <q-btn dense flat round icon="close" color="white" v-close-popup />
      </q-bar>

      <q-card-section>
        <p class="text-h5"><strong>Dear XeroLinux users,</strong></p>
        <p>
          It's with a heavy heart that I say this. But after considerable back
          and forth, I have decided that, in May, moving forward, there will
          only be KDE version. XFCE has been <strong>archived</strong>, it is
          <strong>no longer</strong> be available for the public. Nor will there
          be any other DE in the future.
        </p>

        <p>
          The beauty of Linux is, even if an edition is archived, and you like
          it or are using it, you can keep using it with no interruption. It
          just won't be maintained anymore.
        </p>

        <p>
          I didn't want to do this, but with recent pressures to maintain more
          than one edition, with the lack of man power, I cannot do this alone.
          I am constantly trying to, failing miserably.
        </p>

        <p>
          I want to concentrate on one DE, KDE in my case, making it best it
          could be and more. Many Distros only have a single DE and they are
          doing great.... So that's the path I chose.
        </p>

        <p>
          I am so sorry for this. Please do understand, I am but one old man
          doing this... Not a team...
        </p>

        <p>
          Also XeroLinux is a young Distro, not a yet a year old. They do say
          that first year is the rockiest...
        </p>

        <p>Thank you all for your continued support</p>
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
import Features from "src/components/sections/Features.vue";

import { defineComponent, ref } from "vue";

export default defineComponent({
  name: "PageIndex",
  components: {
    About,
    Hero,
    Download,
    Customization,
    AnnouncementBanner,
    Features,
  },
  setup() {
    const popup = ref(false);
    return {
      popup,
    };
  },
});
</script>

<style lang="scss" scoped>
.new-user {
  max-width: 80vw;
  flex-grow: 1;
}
</style>
