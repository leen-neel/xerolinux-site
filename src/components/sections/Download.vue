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
          .:: Download XeroLinux ::.
        </div>
      </div>

      <div
        class="q-mt-lg"
        :class="{ row: $q.screen.gt.sm, column: $q.screen.lt.md }"
      >
        <div class="col-6 q-mt-md">
          <p
            class="text-justify"
            :class="{
              'width-control': $q.screen.gt.sm,
            }"
            v-html="info.desc"
          ></p>
          <!-- These buttons appear under the description on desktop -->
          <div
            v-if="$q.screen.gt.sm && selectedEditionID !== 'gnome'"
            class="row q-mt-md q-gutter-sm"
          >
            <q-btn
              label="Download now"
              icon="download"
              color="accent"
              class="q-ma-sm"
              type="a"
              :href="info.downloadLink"
              target="_blank"
            />

            <q-btn
              label="Release notes"
              color="accent"
              class="q-ma-sm"
              icon="note"
              type="a"
              :href="info.releaseNotes"
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
            <q-video :src="info.yt" class="q-mb-md" id="video-monitor" />
            <!-- These buttons appear below the video on phone -->
            <div
              v-if="$q.screen.lt.md && selectedEditionID !== 'gnome'"
              class="row q-mt-md q-gutter-sm"
              :class="{ 'flex flex-center': $q.screen.lt.md }"
            >
              <q-btn
                label="Release notes"
                color="accent"
                class="q-ma-sm"
                icon="note"
                type="a"
                :href="info.releaseNotes"
                target="_blank"
              />
              <q-btn
                label="Download now"
                icon="download"
                color="accent"
                class="q-ma-sm"
                type="a"
                :href="info.downloadLink"
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

    const info = ref({
      name: "KDE",
      desc: '<p>This is our "Flagship" release, it uses KDE as its DE and offers a wide variety of packages to choose from during install, support for a wide host of Hardware, not to mention the level of customisation that KDE brings with it.</p> <p>This edition will be the one we will be concentrating most our efforts on, and the one that will have the biggest amount of features. It will be getting some cool standalone rices that you will be able to install with minimal effort as well as many other features.</p>',
      downloadLink:
        "https://sourceforge.net/projects/xerolinux/files/Releases/Main/xerolinux-main-x86_64.iso/download",
      releaseNotes: "https://forum.xerolinux.xyz/thread-4.html",
      yt: "https://www.youtube.com/embed/lGw7lspuTPo?rel=0",
    });

    return {
      selectedEditionID,
      info,
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
