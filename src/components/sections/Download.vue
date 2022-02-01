<template>
  <section id="download" class="q-pa-md">
    <h2 class="text-center">Download</h2>

    <h4 class="text-bold">XeroLinux {{ editions[selectedEditionID].name }}</h4>
    <div :class="{ row: $q.screen.gt.sm, column: $q.screen.lt.md }">
      <div class="col-6">
        <p>
          {{ editions[selectedEditionID].desc }}
        </p>

        <div class="row q-gutter-sm">
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

        <div class="text-h4 q-mt-md">Other Edtitions</div>
        <div class="row q-gutter-sm q-mt-sm">
          <q-btn
            v-if="selectedEditionID !== 'kde'"
            label="KDE"
            color="accent"
            @click="selectedEditionID = 'kde'"
          />
          <q-btn
            v-if="selectedEditionID !== 'gnome'"
            label="GNOME"
            color="accent"
            @click="selectedEditionID = 'gnome'"
          />
          <q-btn
            v-if="selectedEditionID !== 'xfce'"
            label="XFCE"
            color="accent"
            @click="selectedEditionID = 'xfce'"
          />
        </div>
      </div>

      <div
        class="col-6"
        :class="{ 'flex flex-center q-mt-md': $q.screen.lt.md }"
      >
        <div>
          <q-video
            src="https://www.youtube.com/embed/IQn9LGyAJJ8?rel=0"
            class="q-mb-md"
            id="video-monitor"
          />
          <div class="flex flex-center">
            <div class="stand"></div>
          </div>
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
      },

      xfce: {
        name: "XFCE",
        desc: "While this one was created for all of you out there that don't have powerful enough hardware to run our \"Flagship\" release that uses tons of effects and other tools that use a lot of system resources. It uses XFCE as its DE, as it's one of the lightest out there, that can still be made to look great without impacting performance. Don't worry though, it still retains most of the main features but with a bit less options.",
        downloadLink:
          "https://sourceforge.net/projects/xerolinux/files/Releases/XFCE/xerolinux-xfce-x86_64.iso/download",
        releaseNotes: "https://forum.xerolinux.xyz/thread-14.html",
      },

      gnome: {
        name: "GNOME",
        desc: "This was requested hard on both Discord and Telegram. I succumb to the pressure and released it. It fully supports Wayland on nVidia cards, that's the biggest part. Otherwise it's just basic, I opted not to use too many extensions as GNOME is notorious for having them break with every major upgrade. So in essence this edition only exists because of it being requested so hard. A new version will only be released on major events like, New Year's, Valentine's, Easter, Thanksgiving and Christmas. Not as frequently as the others. This is the last edition to be added to the family. I hope you like it.",
        downloadLink:
          "https://sourceforge.net/projects/xerolinux/files/Releases/GNOME/xerolinux-gnome-x86_64.iso/download",
        releaseNotes: "https://forum.xerolinux.xyz/thread-66.html",
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
.header {
  height: 50vh;
  background-image: linear-gradient(
      180deg,
      rgba(40, 42, 54, 0.208) 41.04%,
      rgba(40, 42, 54, 0.95) 89.87%
    ),
    url(/images/hero.jpg);
  background-position: top center;
  background-repeat: no-repeat;
  background-size: cover;
}

#video-monitor {
  border: 15px solid black;
  border-radius: 8px;
}
</style>
