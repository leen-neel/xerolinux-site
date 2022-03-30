<template>
  <div
    id="about"
    :class="{
      'text-h2': $q.screen.gt.sm,
      'text-h4 text-bold': $q.screen.lt.md,
    }"
    class="q-mt-sm text-center q-pa-sm"
  >
    About XeroLinux
  </div>

  <div class="flex flex-center">
    <div
      class="text-justify q-pa-md q-mt-sm"
      :class="{
        'about-desc': $q.screen.gt.sm,
      }"
    >
      <p>
        This is XeroLinux - an Arch-based Distro, a personal project I am
        working on that I thought I would share, in case someone out there
        shares my passion for building Linux.
      </p>
      <p class="q-mt-lg">
        I have created it for myself first and foremost, as a hobby, in my spare
        time, to learn the inner workings of Linux, which means it's mainly
        compatible with the hardware I currently own.
      </p>
      <div class="disclaimer text-lg">
        Disclaimer, please
        <q-btn color="primary" label="Read" @click="popup = true" size="md" />
      </div>
      <p>
        The beauty of Linux is, you can fix various issues yourself, with enough
        knowledge.
      </p>

      <p class="q-mt-lg">As the saying goes...</p>
      <q-card class="my-card">
        <q-card-section>
          <strong
            >"If you can't find the best Distro for you, then BUILD YOUR
            OWN!".</strong
          >
          That's the power of ArchLinux.
        </q-card-section>
      </q-card>
    </div>
  </div>

  <!-- FAQs -->
  <q-dialog v-model="popup" class="z-top">
    <q-card class="radius-16 bg-red-9" style="width: 85%; max-width: 90vw">
      <q-bar dark class="text-white">
        <q-space />
        <q-btn dense flat round icon="close" color="white" v-close-popup />
      </q-bar>

      <q-card-section>
        <p class="text-h4"><strong>XeroLinux Disclaimer</strong></p>
        <p>
          Please read this carefully to understand more about what this project
          is and what it entails.
        </p>
      </q-card-section>

      <q-card-section>
        <div class="text-weight-bold q-mb-md text-h5">Disclaimer</div>
        <p>
          This Distro is a private project that I have created for myself first
          and foremost, as a hobby, in my spare time, to learn the inner
          workings of Linux, which means it's mainly compatible with the
          hardware I currently own. Also it was never built to replace the likes
          of Manjaro, Garuda, Arco etc...
        </p>
        <p>
          The beauty of Linux is, you can fix various issues yourself, with
          enough knowledge.
        </p>
      </q-card-section>

      <q-card-section>
        <div class="text-weight-bold q-mb-md text-h5">
          What does it mean for you?
        </div>
        <p>
          When it comes to issues related to your specific hardware config, you
          better be ready to do your own research using the awesome knowledge
          found on ArchWiki and/or the Web. You can help others by sharing
          solutions, power of the community
        </p>
        <p>
          Otherwise, we will do best we can to assist you. If not myself, other
          users might be able to chime in if and when they can. All I ask for is
          a lot of patience as I am one man doing this, not a team.
        </p>
      </q-card-section>

      <q-card-section>
        <div class="text-weight-bold q-mb-md text-h5">
          No DE Requests Accepted
        </div>
        <p>
          I won't be adding other DEs, KDE is and forever will be only one
          moving forward. I won't be accepting requests for any. I cannot
          stretch myself too thin. I am doing it for the fun of learning.
        </p>
      </q-card-section>

      <q-card-section>
        <div class="text-weight-bold q-mb-md text-h5">
          AUR Packages on Xero Repos
        </div>
        <p>
          While you can request packages from AUR to be built and added to our
          repos, but if they depend on any other DE than KDE they will be
          rejected.
        </p>
      </q-card-section>

      <q-card-section>
        <div class="text-weight-bold q-mb-md text-h5">
          What will NOT be supported
        </div>
        <p>
          We will NOT provide support for the following scenarios, please take
          that however you want, just as long as you are good with it.
        </p>
      </q-card-section>

      <q-card-section>
        <li>Hack Installs.</li>
        <li>Cloud Server Installs.</li>
        <li>Installs on Apple devices.</li>
        <li>Other Installed DEs or WMs.</li>
        <li>Installs on Tablets and other Touch devices.</li>
      </q-card-section>

      <q-card-section>
        I hope this clarifies the matter once and for all..
      </q-card-section>

      <q-card-section>
        <p>XeroLinux Admin/Creator.</p>
      </q-card-section>
    </q-card>
  </q-dialog>
  <!-- End of FAQs -->
</template>

<script>
import { ref, defineComponent } from "vue";

export default defineComponent({
  setup() {
    const popup = ref(false);

    return {
      popup,
    };
  },
});
</script>

<style lang="scss">
.about-desc {
  max-width: 97.5vw;
  background-color: #44475a;
  border-radius: 16px;
  margin-bottom: 10px;

  .q-card {
    background-color: #313341;
  }
}

.line-icon {
  box-sizing: border-box;
  position: relative;
  text-align: center;
  background-image: url("/images/logoIcon.png");
  background-repeat: no-repeat;
  background-position: center;
  font-size: 0;
  height: 40px;
}
.line-icon::before,
.line-icon::after {
  box-sizing: border-box;
  width: 40%;
  height: 1px;
  border-top: 1px solid #d6d6d6;
  display: inline-block;
  content: "";
  margin-left: 5%;
  margin-right: 5%;
  position: relative;
  top: 50%;
  -moz-transform: translatey(-50%);
  -ms-transform: translatey(-50%);
  -o-transform: translatey(-50%);
  -webkit-transform: translatey(-50%);
  transform: translatey(-50%);
}

.disclaimer {
  overflow: hidden;
  text-align: center;
  margin: 20px 0 20px 0;
}

.disclaimer:before,
.disclaimer:after {
  background-color: #d6d6d6;
  content: "";
  display: inline-block;
  height: 1px;
  position: relative;
  vertical-align: middle;
  width: 50%;
}

.disclaimer:before {
  right: 0.5em;
  margin-left: -50%;
}

.disclaimer:after {
  left: 0.5em;
  margin-right: -50%;
}
</style>
