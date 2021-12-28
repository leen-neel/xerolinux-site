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
        col-xs-12 col-sm-6 col-md-4
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
          <div class="text-h3 text-center header">XeroLinux Main</div>
        </q-card-section>
        <q-card-section>
          This is our "Flagship" release. It uses KDE as its DE with a lot going
          on in the <em>EyeCandy</em> department. It also offers more package
          options during install, supports more Hardware, like Surface laptops,
          Wacom tablets and more. It also has a more fully featured Post-Install
          tool. Not meant for Low-End hardware.
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
      <!-- XFCE -->

      <q-card class="edition-card card-2 radius-16">
        <q-img
          src="https://i.imgur.com/TDU3Hgd.png"
          spinner-color="primary"
          spinner-size="82px"
        />
        <q-card-section>
          <div class="text-h3 text-center header">XeroLinux XFCE</div>
        </q-card-section>
        <q-card-section>
          You don't have powerful enough hardware to enjoy our flagship release
          which uses KDE with a lot of resource hungry effects and tools? Then
          this edition is for you. It has most of the
          <em>Flagship's</em> features, but we toned down the effects, and it's
          running one of the lightest and still customizable DEs out there
          <strong>XFCE.</strong>
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

      <!-- XFCE -->

      <q-card class="edition-card card-2 radius-16">
        <q-img
          src="https://images-ext-1.discordapp.net/external/C2zz9ZR6x4x45NPjB2_kYcT_zioiM2SBSKbqIxbaHkc/https/media.discordapp.net/attachments/910111834206511175/925071385951358986/unknown.png"
          spinner-color="primary"
          spinner-size="82px"
        />
        <q-card-section>
          <div class="text-h3 text-center header">XeroLinux GNOME</div>
        </q-card-section>
        <q-card-section>
          You have nVidia and want to benefit from Wayland ? Have powerful
          hardware, and prefer GNOME over other DEs ? This is for you. Minimal
          tweaking as GNOME is notorious for having them break with every major
          upgrade. A new version will only be released on major events like, New
          Year's, Valentine's, Easter, Thanksgiving and Christmas. Not as
          frequently as the others. This is the last edition to be added to the
          family. I hope you like it.
        </q-card-section>

        <q-card-actions align="center">
          <q-badge
            color="negative"
            class="text-weight-bolder text-h6 announcement-badge"
          >
            Coming soon
          </q-badge>
        </q-card-actions>

        <q-card-actions v-if="false" class="row justify-evenly">
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
  max-width: 600px;
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
