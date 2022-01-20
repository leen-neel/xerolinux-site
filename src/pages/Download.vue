<template>
  <q-page>
    <section class="header flex flex-center">
      <h2>Download</h2>
    </section>

    <section class="q-pa-md">
      <h2>XeroLinux KDE</h2>
      <div class="row">
        <div class="col-6">
          <p>
            This is our "Flagship" release, it uses KDE as its DE and offers a
            wide variety of packages to choose from during install, support for
            a wide host of Hardware, not to mention the level of customisation
            that KDE brings with it.
          </p>

          <div class="row q-gutter-sm">
            <q-btn
              label="Full Release notes"
              color="accent"
              class="q-ma-sm"
              icon="note"
              type="a"
              href="https://forum.xerolinux.xyz/thread-4.html"
              target="_blank"
            />
            <q-btn
              label="Download now"
              icon="download"
              color="accent"
              class="q-ma-sm"
              type="a"
              href="https://sourceforge.net/projects/xerolinux/files/Releases/Main/xerolinux-main-x86_64.iso/download"
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
            <q-btn label="KDE" color="accent" />
            <q-btn label="GNOME" color="accent" />
            <q-btn label="XFCE" color="accent" />
          </div>
        </div>

        <div class="col-6">
          <div id="video-laptop">
            <iframe
              width="560"
              height="390"
              src="https://www.youtube.com/embed/S_QemrZbOIk"
              frameborder="0"
              allowfullscreen
            ></iframe>
          </div>
        </div>
      </div>
    </section>
  </q-page>
</template>

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

#video-laptop {
  position: relative;
  padding-top: 25px;
  padding-bottom: 67.5%;
  height: 0;

  iframe {
    box-sizing: border-box;
    background: url(http://i.stack.imgur.com/zZNgk.png) center center no-repeat;
    background-size: contain;
    padding: 11.9% 15.5% 14.8%;
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
  }
}
</style>
