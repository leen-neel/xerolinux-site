<template>
  <div id="editions" class="text-h2 q-mt-sm text-center q-pa-sm">
    XeroLinux Editions
  </div>

  <div
    class="
      row
      flex-center
      q-gutter-md q-mt-sm
      col-xs-12 col-sm-6 col-md-4
      q-pa-sm
    "
  >
    <!-- Main -->
    <q-card class="edition-card">
      <q-img
        src="https://i.imgur.com/TNg4vJr.jpeg"
        spinner-color="primary"
        spinner-size="82px"
      />
      <q-card-section>
        <div class="text-h3">XeroLinux Main</div>
      </q-card-section>
      <q-card-section>
        This one is a bit long in the tooth to describe, suffice it to say that
        this one is where you get all the bells and whistles. It's got so many
        that you will HAVE to read the entire Release notes to get the big
        picture.
      </q-card-section>

      <div class="text-center text-positive">~[Features in a nutshell]~</div>
      <q-card-section class="row">
        <div class="col-6">
          <q-list>
            <q-item>
              <q-item-section class="q-mr-sm" side>
                <q-icon color="white" name="arrow_forward" />
              </q-item-section>
              <q-item-section> Intel VMD™ support </q-item-section>
            </q-item>

            <q-item>
              <q-item-section class="q-mr-sm" side>
                <q-icon color="white" name="arrow_forward" />
              </q-item-section>
              <q-item-section> "nVidia" On Boot </q-item-section>
            </q-item>

            <q-item>
              <q-item-section class="q-mr-sm" side>
                <q-icon color="white" name="arrow_forward" />
              </q-item-section>
              <q-item-section> Wayland Support </q-item-section>
            </q-item>

            <q-item>
              <q-item-section class="q-mr-sm" side>
                <q-icon color="white" name="arrow_forward" />
              </q-item-section>
              <q-item-section> PipeWire/PulseAudio </q-item-section>
            </q-item>

            <q-item>
              <q-item-section class="q-mr-sm" side>
                <q-icon color="white" name="arrow_forward" />
              </q-item-section>
              <q-item-section> Wacom Tablet support </q-item-section>
            </q-item>
          </q-list>
        </div>

        <div class="col-6">
          <q-list>
            <q-item>
              <q-item-section class="q-mr-sm" side>
                <q-icon color="white" name="arrow_forward" />
              </q-item-section>
              <q-item-section> New SysConfig Tool </q-item-section>
            </q-item>

            <q-item>
              <q-item-section class="q-mr-sm" side>
                <q-icon color="white" name="arrow_forward" />
              </q-item-section>
              <q-item-section> Refreshed Rice </q-item-section>
            </q-item>

            <q-item>
              <q-item-section class="q-mr-sm" side>
                <q-icon color="white" name="arrow_forward" />
              </q-item-section>
              <q-item-section> Paru (AUR) helper </q-item-section>
            </q-item>

            <q-item>
              <q-item-section class="q-mr-sm" side>
                <q-icon color="white" name="arrow_forward" />
              </q-item-section>
              <q-item-section> Package selection </q-item-section>
            </q-item>

            <q-item>
              <q-item-section class="q-mr-sm" side>
                <q-icon color="white" name="arrow_forward" />
              </q-item-section>
              <q-item-section> And more.... </q-item-section>
            </q-item>
          </q-list>
        </div>
      </q-card-section>

      <q-card-actions class="row justify-evenly q-ma-sm">
        <q-btn
          label="Full Release notes"
          color="accent"
          class="btn"
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
          class="btn"
          type="a"
          href="https://sourceforge.net/projects/xerolinux/files/Releases/Main/xerolinux-main-2021.11-x86_64.iso/download"
          target="_blank"
          style="font-size: 13px"
        />

        <q-btn
          label="Installation guide"
          color="accent"
          icon="fas fa-file-download"
          class="btn"
          type="a"
          href="https://forum.xerolinux.xyz/thread-38.html"
          target="_blank"
          style="font-size: 13px"
        />
      </q-card-actions>
    </q-card>

    <!-- Core -->
    <q-card class="edition-card">
      <q-img
        src="https://i.imgur.com/27KxEm6.jpeg"
        spinner-color="primary"
        spinner-size="82px"
      />
      <q-card-section>
        <div class="text-h3">XeroLinux Core</div>
      </q-card-section>
      <q-card-section>
        It’s a stripped down version of the main release. Yes, this will not
        have the fancy look that main edition has, nor does it have any of the
        bells n whistles. But it still retains the Driver selector page for best
        compatibility.
      </q-card-section>

      <div class="text-center text-positive">~[Features in a nutshell]~</div>

      <q-card-section class="row">
        <div class="col-6">
          <q-list>
            <q-item>
              <q-item-section class="q-mr-sm" side>
                <q-icon color="white" name="arrow_forward" />
              </q-item-section>
              <q-item-section> Arch/Vanilla KDE </q-item-section>
            </q-item>

            <q-item>
              <q-item-section class="q-mr-sm" side>
                <q-icon color="white" name="arrow_forward" />
              </q-item-section>
              <q-item-section> Neofetch Activated </q-item-section>
            </q-item>

            <q-item>
              <q-item-section class="q-mr-sm" side>
                <q-icon color="white" name="arrow_forward" />
              </q-item-section>
              <q-item-section> Intel VMD™ support </q-item-section>
            </q-item>

            <q-item>
              <q-item-section class="q-mr-sm" side>
                <q-icon color="white" name="arrow_forward" />
              </q-item-section>
              <q-item-section> "nVidia" On Boot </q-item-section>
            </q-item>
          </q-list>
        </div>

        <div class="col-6">
          <q-list>
            <q-item>
              <q-item-section class="q-mr-sm" side>
                <q-icon color="white" name="arrow_forward" />
              </q-item-section>
              <q-item-section> Paru (AUR) helper </q-item-section>
            </q-item>

            <q-item>
              <q-item-section class="q-mr-sm" side>
                <q-icon color="white" name="arrow_forward" />
              </q-item-section>
              <q-item-section> Wayland Support </q-item-section>
            </q-item>

            <q-item>
              <q-item-section class="q-mr-sm" side>
                <q-icon color="white" name="arrow_forward" />
              </q-item-section>
              <q-item-section> And more.... </q-item-section>
            </q-item>
          </q-list>
        </div>
      </q-card-section>

      <q-card-actions class="row justify-evenly q-ma-sm">
        <q-btn
          label="Full Release notes"
          color="accent"
          class="btn"
          icon="note"
          type="a"
          href="https://forum.xerolinux.xyz/thread-14.html  "
          target="_blank"
          style="font-size: 13px"
        />

        <q-btn
          label="Download now"
          icon="download"
          color="accent"
          class="btn"
          type="a"
          href=" https://sourceforge.net/projects/xerolinux/files/Releases/Core/xerolinux-core-2021.11-x86_64.iso/download"
          target="_blank"
          style="font-size: 13px"
        />

        <q-btn
          label="Installation guide"
          color="accent"
          icon="fas fa-file-download"
          class="btn"
          type="a"
          href="https://forum.xerolinux.xyz/thread-38.html"
          target="_blank"
          style="font-size: 13px"
        />
      </q-card-actions>
    </q-card>
  </div>
</template>

<style lang="scss" scoped>
.edition-card {
  max-width: 600px;
}
</style>
