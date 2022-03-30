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
          <div v-if="$q.screen.gt.sm" class="row q-mt-md q-gutter-sm">
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
              label="FAQs"
              color="accent"
              class="q-ma-sm"
              icon="help_outline"
              @click="popup = true"
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
              v-if="$q.screen.lt.md"
              class="row q-mt-md q-gutter-sm"
              :class="{ 'flex flex-center': $q.screen.lt.md }"
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
                label="FAQs"
                color="accent"
                class="q-ma-sm"
                icon="help_outline"
                @click="popup = true"
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
          XeroLinux was born as a KDE only Distro. No WMs please, do not request
          any. The more I add the further it will drift from original vision of
          do one thing and do it good.
        </p>
      </q-card-section>

      <q-card-section>
        <ul>
          <li>
            <a
              href="https://forum.xerolinux.xyz/thread-38.html"
              target="_blank"
              rel="noopener noreferrer"
              >Installing for 1st time? Follow instructions closely</a
            >
          </li>

          <li>
            <a
              href="https://forum.xerolinux.xyz/thread-28.html"
              target="_blank"
              rel="noopener noreferrer"
              >Having issues? This is where I store solutions</a
            >
          </li>

          <li>
            <a
              href="https://forum.xerolinux.xyz/thread-67.html"
              target="_blank"
              rel="noopener noreferrer"
            >
              Wanna get latest features without reinstall?</a
            >
          </li>

          <li>
            <a
              href="https://forum.xerolinux.xyz/thread-7.html"
              target="_blank"
              rel="noopener noreferrer"
            >
              Own "Legacy" nVidia GPU?</a
            >
          </li>

          <li>
            <a
              href="https://forum.xerolinux.xyz/thread-75.html"
              target="_blank"
              rel="noopener noreferrer"
            >
              Having WiFi freezing issue?</a
            >
          </li>

          <li>
            <a
              href="https://forum.xerolinux.xyz/thread-5.html"
              target="_blank"
              rel="noopener noreferrer"
            >
              Want to DualBoot with Windows?</a
            >
          </li>

          <li>
            <a
              href="https://forum.xerolinux.xyz/thread-80.html"
              target="_blank"
              rel="noopener noreferrer"
            >
              Wanna learn more about Snapper?</a
            >
          </li>

          <li>
            <a
              href="https://forum.xerolinux.xyz/thread-19.html"
              target="_blank"
              rel="noopener noreferrer"
            >
              Learn my terminal Aliases here</a
            >
          </li>

          <li>
            <a
              href="https://forum.xerolinux.xyz/thread-90.html"
              target="_blank"
              rel="noopener noreferrer"
            >
              Stuck with vmlinuz-linux not found?</a
            >
          </li>

          <li>
            <a
              href="https://forum.xerolinux.xyz/thread-87.html"
              target="_blank"
              rel="noopener noreferrer"
            >
              Issues updating due to failed mirrors (404)?</a
            >
          </li>
        </ul>
      </q-card-section>

      <q-card-section>
        <p>
          Thank you,
          <br />
          XeroLinux Dev
        </p>
      </q-card-section>
    </q-card>
  </q-dialog>
</template>

<script>
import { ref, defineComponent } from "vue";

export default defineComponent({
  setup() {
    const popup = ref(false);

    const info = ref({
      name: "KDE",
      desc: "<p>This is XeroLinux KDE, offers a wide variety of packages to choose from during install, not to mention the level of customization that KDE brings with it.</p> <p>It offers freedom of choice. It also has some cool standalone rices (customization section) that you will be able to install with minimal effort as well as the <strong>XeroLinux Tool</strong>, and much much more...</p>",
      downloadLink:
        "https://sourceforge.net/projects/xerolinux/files/Releases/Main/xerolinux-main-x86_64.iso/download",
      releaseNotes: "https://forum.xerolinux.xyz/thread-4.html",
      yt: "https://www.youtube.com/embed/rqCTzdLNeXY?rel=0",
    });

    return {
      info,
      popup,
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
