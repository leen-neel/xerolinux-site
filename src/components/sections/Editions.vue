<template>
  <section class="edition-bg q-pa-sm">
    <div id="editions" class="bg-blur text-h3 q-mt-sm text-center q-pa-sm">
      XeroLinux Editions
    </div>
    <div
      class="
        row
        flex-center
        q-gutter-md q-my-md
        col-xs-12 col-sm-2 col-md-2
        q-pa-sm
      "
    >
      <!-- Main -->
      <q-card class="edition-card card-1 radius-16">
        <q-img
          src="https://cdn.discordapp.com/attachments/912888928749645896/917800804096806942/New.jpg"
          spinner-color="primary"
          spinner-size="82px"
        />
        <q-card-section>
          <div class="text-h4 text-center header">XeroLinux Main</div>
        </q-card-section>

        <q-card-actions class="row justify-evenly q-pa-sm">
          <q-btn
            label="Full Release notes"
            color="accent"
            class="btn q-ma-sm"
            icon="note"
            type="a"
            href="https://forum.xerolinux.xyz/thread-4.html"
            target="_blank"
            style="font-size: 13px"
          />
          <q-btn
            label="Download now"
            icon="download"
            color="accent"
            class="btn q-ma-sm"
            type="a"
            href="https://sourceforge.net/projects/xerolinux/files/Releases/Main/xerolinux-main-x86_64.iso/download"
            target="_blank"
            style="font-size: 13px"
          />
          <q-btn
            label="Installation guide"
            color="accent"
            icon="fas fa-file-download"
            class="btn q-ma-sm"
            type="a"
            href="https://forum.xerolinux.xyz/thread-38.html"
            target="_blank"
            style="font-size: 13px"
          />
        </q-card-actions>
      </q-card>

      <!-- GNOME -->

      <q-card class="edition-card card-3 radius-16">
        <q-img
          src="https://images-ext-1.discordapp.net/external/C2zz9ZR6x4x45NPjB2_kYcT_zioiM2SBSKbqIxbaHkc/https/media.discordapp.net/attachments/910111834206511175/925071385951358986/unknown.png"
          spinner-color="primary"
          spinner-size="82px"
        />
        <q-card-section>
          <div class="text-h4 text-center header">XeroLinux GNOME</div>
        </q-card-section>

        <q-card-actions v-if="true" class="row justify-evenly">
          <q-btn
            label="Coming soon"
            color="accent"
            class="btn q-ma-sm"
            icon="note"
            style="font-size: 13px"
          />
          <q-btn
            label="Coming soon"
            icon="download"
            color="accent"
            class="btn q-ma-sm"
            style="font-size: 13px"
          />
          <q-btn
            label="Installation guide"
            color="accent"
            icon="fas fa-file-download"
            class="btn q-ma-sm"
            type="a"
            href="https://forum.xerolinux.xyz/thread-38.html"
            target="_blank"
            style="font-size: 13px"
          />
        </q-card-actions>
      </q-card>

      <!-- XFCE -->

      <q-card class="edition-card card-2 radius-16">
        <q-img
          src="https://i.imgur.com/TDU3Hgd.png"
          spinner-color="primary"
          spinner-size="82px"
        />
        <q-card-section>
          <div class="text-h4 text-center header">XeroLinux XFCE</div>
        </q-card-section>

        <q-card-actions class="row justify-evenly">
          <q-btn
            label="Full Release notes"
            color="accent"
            class="btn q-ma-sm"
            icon="note"
            type="a"
            href="https://forum.xerolinux.xyz/thread-14.html"
            target="_blank"
            style="font-size: 13px"
          />
          <q-btn
            label="Download now"
            icon="download"
            color="accent"
            class="btn q-ma-sm"
            type="a"
            href="https://sourceforge.net/projects/xerolinux/files/Releases/XFCE/xerolinux-xfce-x86_64.iso/download"
            target="_blank"
            style="font-size: 13px"
          />
          <q-btn
            label="Installation guide"
            color="accent"
            icon="fas fa-file-download"
            class="btn q-ma-sm"
            type="a"
            href="https://forum.xerolinux.xyz/thread-38.html"
            target="_blank"
            style="font-size: 13px"
          />
        </q-card-actions>
      </q-card>
    </div>
  </section>
</template>

<style lang="scss">
.edition-card {
  max-width: 420px;
  background: rgba(40, 42, 54, 0.3);
  backdrop-filter: blur(15px);
  -webkit-backdrop-filter: blur(15px);
}

.card-1 {
  font-size: 17.09px;
}

.card-2 {
  font-size: 17.09px;
}

@media (max-width: $breakpoint-xs-max) {
  .edition-card,
  .features {
    font-size: 10px;
  }

  .card-2 {
    font-size: 10px;
  }

  .header {
    text-align: center;
  }

  .header {
    font-size: 28px;
    text-align: center;
  }
}
</style>
