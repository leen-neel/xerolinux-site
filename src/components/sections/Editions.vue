<template>
  <section class="edition-bg">
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
            to="/mainreleasenotes"
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
      <!-- Core -->

      <q-card class="edition-card card-2 radius-16">
        <q-img
          src="https://cdn.discordapp.com/attachments/912888928749645896/920342867115909120/unknown.png"
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

        <q-card-section class="q-ma-none">
          <div class="text-h5 text-center">
            <q-badge color="negative" class="text-h6 text-weight-bolder">
              Coming soon!
            </q-badge>
          </div>
        </q-card-section>
        <!-- type="a"
            href="https://forum.xerolinux.xyz/thread-14.html"
            target="_blank" -->
        <q-card-actions v-if="false" class="row justify-evenly">
          <q-btn
            label="Full Release notes"
            color="accent"
            class="btn q-ma-sm"
            icon="note"
            to="/mainreleasenotes"
            style="font-size: 13px"
          />
          <q-btn
            label="Download now"
            icon="download"
            color="accent"
            class="btn q-ma-sm"
            type="a"
            href="https://sourceforge.net/projects/xerolinux/files/Releases/Core/xerolinux-core-x86_64.iso/download"
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
