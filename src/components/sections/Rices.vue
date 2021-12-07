<template>
  <q-card class="rice-card radius-16">
    <q-img
      src="https://imgur.com/qwurLBg.jpeg"
      spinner-color="primary"
      spinner-size="82px"
    />

    <q-card-section>
      <div class="text-h3 text-center header">Rices</div>
    </q-card-section>

    <q-card-actions vertical align="center">
      <q-btn
        label="XeroLayan"
        color="accent"
        class="btn q-ma-sm"
        @click="xerolayan = true"
        target="_blank"
        style="font-size: 13px"
      />

      <div class="row">
        <q-btn
          label="XeroDracul"
          color="accent"
          class="btn q-ma-sm"
          @click="xerodracul = true"
          style="font-size: 13px"
        />

        <q-btn
          label="XeroNord"
          color="accent"
          class="btn q-ma-sm"
          @click="xeronord = true"
          style="font-size: 13px"
        />
        <q-btn
          label="XeroSweet"
          color="accent"
          class="btn q-ma-sm"
          @click="xerosweet = true"
          style="font-size: 13px"
        />
      </div>
    </q-card-actions>
  </q-card>

  <!-- XeroLayan -->
  <q-dialog
    v-model="xerolayan"
    transition-show="slide-up"
    transition-hide="slide-down"
    class="z-top"
  >
    <Rice
      img="https://i.imgur.com/5uvZjUf.jpeg"
      name="XeroLayan"
      link="https://github.com/xerolinux/xero-layan-git"
    >
      This rice is the main one used on my Distro, uses Latte for both Panels &
      Dock. It is intended to be mainly used on XeroLinux. I made scripts to
      install on "Debian" (KDENeon) and "Fedora KDE Spin"... Test it out and let
      me know...
    </Rice>
  </q-dialog>

  <!-- XeroDracul -->
  <q-dialog
    v-model="xerodracul"
    transition-show="slide-up"
    transition-hide="slide-down"
    class="z-top"
  >
    <Rice
      img="https://i.imgur.com/qwurLBg.jpeg"
      name="XeroDracul"
      link="https://github.com/xerolinux/xero-dracul-git"
    >
      This rice is a bit complex, uses Latte for everything including side bars.
      It is intended to be mainly used on XeroLinux. Also is based on the
      Dracula Theme hence the name. Have fun.
    </Rice>
  </q-dialog>

  <!-- XeroSweet -->
  <q-dialog
    v-model="xerosweet"
    transition-show="slide-up"
    transition-hide="slide-down"
    class="z-top"
  >
    <Rice
      img="https://i.imgur.com/qRm0ooD.jpg"
      name="XeroSweet"
      link="https://github.com/xerolinux/xero-sweet-git"
    >
      This rice is super simple, based on the SweetKDE theme with Candy Icons,
      not very complex easy on resources. It is intended to be mainly used on
      XeroLinux. Have fun.
    </Rice>
  </q-dialog>

  <!-- XeroNord -->
  <q-dialog
    v-model="xeronord"
    transition-show="slide-up"
    transition-hide="slide-down"
    class="z-top"
  >
    <q-card class="bg-dark text-white radius-16">
      <q-video
        style="height: 300px; width: 100%"
        src="https://www.youtube.com/embed/Kh_Mmu4toN8"
      />

      <q-card-section>
        <div class="text-center text-h3">XeroNord</div>
      </q-card-section>

      <q-card-section class="q-pt-none">
        <div class="desc">
          This rice is one of my faves, it's based on the Nordic theme with
          quite a unique layout. Latte all of course. It is intended to be
          mainly used on XeroLinux. Have fun.
        </div>
      </q-card-section>

      <q-card-actions class="q-ma-sm" align="right">
        <q-btn
          type="a"
          target="_blank"
          href=" https://github.com/xerolinux/xero-nord-git"
          color="primary"
          class="q-pa-md"
          label="Installation guide"
        />
      </q-card-actions>
    </q-card>
  </q-dialog>
</template>

<script>
import { ref, defineComponent } from "vue";
import Rice from "../Rice.vue";

export default defineComponent({
  setup() {
    return {
      xerolayan: ref(false),
      xerodracul: ref(false),
      xerosweet: ref(false),
      xeronord: ref(false),
    };
  },
  components: {
    Rice,
  },
});
</script>

<style lang="scss" scoped>
.rice-card {
  width: 600px;
}
</style>
