<template>
  <div id="editions" class="text-h3 q-mt-sm text-center q-pa-sm">
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
    <q-card class="edition-card card-1 radius-16">
      <q-img
        src="https://i.imgur.com/TNg4vJr.jpeg"
        spinner-color="primary"
        spinner-size="82px"
      />
      <q-card-section>
        <div class="text-h3 text-center header">XeroLinux Main</div>
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
              <q-item-section> PipeWire / Pulse </q-item-section>
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
        bells n whistles. But it still retains the Driver selector page for best
        compatibility.
      </q-card-section>

      <div class="text-center text-positive">~[Features in a nutshell]~</div>

      <q-card-section class="row features">
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
              <q-item-section> Neofetch </q-item-section>
            </q-item>

            <q-item>
              <q-item-section class="q-mr-sm" side top>
                <q-icon color="white" name="arrow_forward" />
              </q-item-section>
              <q-item-section> VMD™ support </q-item-section>
            </q-item>

            <q-item>
              <q-item-section class="q-mr-sm" side top>
                <q-icon color="white" name="arrow_forward" />
              </q-item-section>
              <q-item-section> "nVidia" On Boot </q-item-section>
            </q-item>

            <q-item>
              <q-item-section class="q-mr-sm" side>
                <q-icon color="white" name="arrow_forward" />
              </q-item-section>
              <q-item-section> Custom .bashrc </q-item-section>
            </q-item>
          </q-list>
        </div>

        <div class="col-6">
          <q-list>
            <q-item>
              <q-item-section class="q-mr-sm" side top>
                <q-icon color="white" name="arrow_forward" />
              </q-item-section>
              <q-item-section> Paru (AUR) helper </q-item-section>
            </q-item>

            <q-item>
              <q-item-section class="q-mr-sm" side>
                <q-icon color="white" name="arrow_forward" />
              </q-item-section>
              <q-item-section> Driver Selector </q-item-section>
            </q-item>

            <q-item>
              <q-item-section class="q-mr-sm" side top>
                <q-icon color="white" name="arrow_forward" />
              </q-item-section>
              <q-item-section> Wayland Support </q-item-section>
            </q-item>

            <q-item>
              <q-item-section class="q-mr-sm" side>
                <q-icon color="white" name="arrow_forward" />
              </q-item-section>
              <q-item-section> Extremely light </q-item-section>
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
</template>

<style lang="scss">
.edition-card {
  max-width: 600px;
}

.card-1 {
  font-size: 17.09px;
}

.card-2 {
  font-size: 18.8px;
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
