<template>
  <div class="flex flex-center">
    <section
      id="download"
      class="q-pa-md edition-bg radius-16"
      style="width: 97.5vw"
    >
      <div class="flex flex-center column">
        <div
          class="text-center"
          :class="{
            'text-h3': $q.screen.gt.sm,
            'text-h6 text-bold': $q.screen.lt.md,
          }"
        >
          .:: Choose Your Edition ::.
        </div>
        <div class="row q-gutter-lg q-mt-md q-mb-lg">
          <q-btn
            v-if="selectedEditionID !== 'kde'"
            label="KDE"
            color="accent"
            @click="selectedEditionID = 'kde'"
            size="18px"
            class="edition-btn"
          />
          <q-btn
            v-if="selectedEditionID !== 'gnome'"
            label="GNOME"
            color="accent"
            @click="selectedEditionID = 'gnome'"
            size="18px"
            class="edition-btn"
          />
          <q-btn
            v-if="selectedEditionID !== 'xfce'"
            label="XFCE"
            color="accent"
            @click="selectedEditionID = 'xfce'"
            size="18px"
            class="edition-btn"
          />
        </div>
      </div>
      <div class="text-h4 q-mb-sm text-bold">
        XeroLinux {{ editions[selectedEditionID].name }}
      </div>
      <div :class="{ row: $q.screen.gt.sm, column: $q.screen.lt.md }">
        <div class="col-6 q-mt-md">
          <p
            class="text-justify"
            :class="{
              'width-control': $q.screen.gt.sm,
            }"
            v-html="editions[selectedEditionID].desc"
          ></p>
          <!-- These buttons appear under the description on desktop -->
          <div v-if="$q.screen.gt.sm" class="row q-mt-md q-gutter-sm">
            <q-btn
              label="Release notes"
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
        <div class="col-6 flex flex-center">
          <div>
            <!-- Video element -->
            <q-video
              :src="editions[selectedEditionID].yt"
              class="q-mb-md"
              id="video-monitor"
            />
            <!-- These buttons appear below the video on phone -->
            <div
              v-if="$q.screen.lt.md"
              class="row q-mt-md q-gutter-sm"
              :class="{ 'flex flex-center': $q.screen.lt.md }"
            >
              <q-btn
                label="Release notes"
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
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import { ref, defineComponent } from "vue";

export default defineComponent({
  setup() {
    const selectedEditionID = ref("kde");

    const editions = ref({
      kde: {
        name: "KDE",
        desc: '<p>This is our "Flagship" release, it uses KDE as its DE and offers a wide variety of packages to choose from during install, support for a wide host of Hardware, not to mention the level of customisation that KDE brings with it.</p> <p>This edition will be the one we will be concentrating most our efforts on, and the one that will have the biggest amount of features. It will be getting some cool standalone rices that you will be able to install with minimal effort as well as many other features.</p>  <p>Think of it as the mother of all editions 😉</p>',
        downloadLink:
          "https://sourceforge.net/projects/xerolinux/files/Releases/Main/xerolinux-main-x86_64.iso/download",
        releaseNotes: "https://forum.xerolinux.xyz/thread-4.html",
        yt: "https://www.youtube.com/embed/lGw7lspuTPo?rel=0",
      },

      xfce: {
        name: "XFCE",
        desc: "<p>This edition was created for all of you out there that don't have powerful enough hardware to run our \"Flagship\" release that uses tons of effects and other tools that use a lot of system resources. It uses XFCE as its DE, as it's one of the lightest out there, that can still be made to look great without impacting performance.</p> <p>Don't worry though, it still retains most of the main features but with a bit less options. Though it will not be getting any standalone rices, I will aim to keep it up to date with slight changes to rice here n there.</p>",
        downloadLink:
          "https://sourceforge.net/projects/xerolinux/files/Releases/XFCE/xerolinux-xfce-x86_64.iso/download",
        releaseNotes: "https://forum.xerolinux.xyz/thread-14.html",
        yt: "https://www.youtube.com/embed/ew5o5svFEK0?rel=0",
      },

      gnome: {
        name: "GNOME",
        desc: "<p>This Edition is no more. In you are one of the few using it and love GNOME so much, please consider switching to a distro that provides it. Off the top of my head, I can recommend Manjaro, Arco, or even EndeavourOS. Whichever you select they all good. I am so sorry about that. You will find reasons behind my decision in the video to the right of this text. Thanks for understanding...</p> <p>Keep Linux Free y'all...</p>",
        downloadLink:
          "https://sourceforge.net/projects/xerolinux/files/Releases/GNOME/xerolinux-gnome-x86_64.iso/download",
        releaseNotes: "https://forum.xerolinux.xyz/thread-66.html",
        yt: "https://www.youtube.com/embed/1q41katiEa8?rel=0",
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
  overflow-x: hidden;
}

.edition-btn {
  padding: 15px 40px;
}

.width-control {
  max-width: 640px;
}

.q-btn {
  border-radius: 16px;
}
</style>
