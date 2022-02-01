<template>
  <section id="download" class="q-pa-md edition-bg">
    <div class="flex flex-center column">
      <div class="text-center text-h2">.:: Choose Your Edition ::.</div>

      <div class="row q-gutter-sm q-mt-sm q-mb-lg">
        <q-btn
          v-if="selectedEditionID !== 'kde'"
          label="KDE"
          color="accent"
          @click="selectedEditionID = 'kde'"
          size="18px"
        />
        <q-btn
          v-if="selectedEditionID !== 'gnome'"
          label="GNOME"
          color="accent"
          @click="selectedEditionID = 'gnome'"
          size="18px"
        />
        <q-btn
          v-if="selectedEditionID !== 'xfce'"
          label="XFCE"
          color="accent"
          @click="selectedEditionID = 'xfce'"
          size="18px"
        />
      </div>
    </div>

    <div class="text-h4 q-mb-sm text-bold">
      XeroLinux {{ editions[selectedEditionID].name }}
    </div>

    <div :class="{ row: $q.screen.gt.sm, column: $q.screen.lt.md }">
      <div class="col-6">
        <p class="q-mt-md" v-html="editions[selectedEditionID].desc"></p>

        <div class="row q-mt-md q-gutter-sm">
          <q-btn
            label="Full Release notes"
            color="accent"
            class="q-ma-sm"
            icon="note"
            type="a"
            :href="editions[selectedEditionID].releaseNotes"
            target="_blank"
          />
          <q-btn
            label="Download now"
            icon="download"
            color="accent"
            class="q-ma-sm"
            type="a"
            :href="editions[selectedEditionID].downloadLink"
            target="_blank"
          />
          <q-btn
            label="Installation guide"
            color="accent"
            icon="fas fa-file-download"
            class="q-ma-sm"
            type="a"
            href="https://forum.xerolinux.xyz/thread-38.html"
            target="_blank"
          />
        </div>
      </div>

      <div
        class="col-6"
        :class="{ 'flex flex-center q-mt-md': $q.screen.lt.md }"
      >
        <div>
          <q-video
            :src="editions[selectedEditionID].yt"
            class="q-mb-md"
            id="video-monitor"
          />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import { ref, defineComponent } from "vue";

export default defineComponent({
  setup() {
    const selectedEditionID = ref("kde");

    const editions = ref({
      kde: {
        name: "KDE",
        desc: 'This is our "Flagship" release, it uses KDE as its DE and offers a wide variety of packages to choose from during install, support for a wide host of Hardware, not to mention the level of customisation that KDE brings with it.',
        downloadLink:
          "https://sourceforge.net/projects/xerolinux/files/Releases/Main/xerolinux-main-x86_64.iso/download",
        releaseNotes: "https://forum.xerolinux.xyz/thread-4.html",
        yt: "https://www.youtube.com/embed/lGw7lspuTPo?rel=0",
      },

      xfce: {
        name: "XFCE",
        desc: "While this one was created for all of you out there that don't have powerful enough hardware to run our \"Flagship\" release that uses tons of effects and other tools that use a lot of system resources. It uses XFCE as its DE, as it's one of the lightest out there, that can still be made to look great without impacting performance. Don't worry though, it still retains most of the main features but with a bit less options.",
        downloadLink:
          "https://sourceforge.net/projects/xerolinux/files/Releases/XFCE/xerolinux-xfce-x86_64.iso/download",
        releaseNotes: "https://forum.xerolinux.xyz/thread-14.html",
        yt: "https://www.youtube.com/embed/ew5o5svFEK0?rel=0",
      },

      gnome: {
        name: "GNOME",
        desc: "<p>This was requested hard on both Discord and Telegram. I succumb to the pressure and released it. It's just a test for now to see how popular it is. If not so much will get killed off. So please do not rely on it living long. I could at any time decide to stop maintaining it. Will be announced on Social what its fate is. Keep a close eye on there.</p> <p> Thanks for understanding. </p>",
        downloadLink:
          "https://sourceforge.net/projects/xerolinux/files/Releases/GNOME/xerolinux-gnome-x86_64.iso/download",
        releaseNotes: "https://forum.xerolinux.xyz/thread-66.html",
        yt: "https://www.youtube.com/embed/DlgXJ3l-Nss?rel=0",
      },
    });

    return {
      selectedEditionID,
      editions,
    };
  },
});
</script>

<style lang="scss" scoped>
#video-monitor {
  border: 15px solid black;
  border-radius: 16px;
}

.q-btn {
  border-radius: 16px;
}
</style>
