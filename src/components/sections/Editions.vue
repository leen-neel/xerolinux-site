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
          This one is a bit long in the tooth to describe, suffice it to say
          that this one is where you get all the bells and whistles. It's got so
          many that you will HAVE to read the entire Release notes to get the
          big picture.
        </q-card-section>
        <q-card-actions class="row justify-evenly">
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
      <!-- Core -->
      <q-card class="edition-card card-2 radius-16">
        <q-img
          src="https://i.imgur.com/27KxEm6.jpeg"
          spinner-color="primary"
          spinner-size="82px"
        />
        <q-card-section>
          <div class="text-h3 text-center header">XeroLinux Core</div>
        </q-card-section>
        <q-card-section>
          It’s a stripped down version of the main release. Yes, this will not
          have the fancy look that main edition has, nor does it have any of the
          bells n whistles. But it still retains the Driver selector page for
          best compatibility.
        </q-card-section>
        <q-card-actions class="row justify-evenly">
          <q-btn
            label="Full Release notes"
            color="accent"
            class="btn q-ma-sm"
            icon="note"
            type="a"
            href="https://forum.xerolinux.xyz/thread-14.htm"
            target="_blank"
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
    font-size: 15px;
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
