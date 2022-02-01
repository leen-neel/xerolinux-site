<template>
  <div class="nav-bg fixed-top row z-top q-pa-md q-gutter-sm">
    <div @click="home" class="cursor-pointer text-h4">XeroLinux</div>

    <q-space />

    <q-btn label="Home" flat style="font-size: 18px" to="/" />
    <q-btn
      v-if="isHome"
      label="About"
      flat
      style="font-size: 18px"
      @click="about"
    />
    <q-btn
      v-if="isHome"
      label="Download"
      flat
      style="font-size: 18px"
      @click="editions"
    />
    <q-btn
      v-if="isHome"
      label="Customization"
      flat
      style="font-size: 18px"
      @click="xeroporn"
    />

    <q-btn
      label="My PC Build"
      flat
      style="font-size: 18px"
      @click="popup = true"
    />

    <q-btn
      label="Forum"
      flat
      style="font-size: 18px"
      type="a"
      href="https://forum.xerolinux.xyz/"
      target="_blank"
      icon-right="open_in_new"
    />
  </div>

  <!-- PC Build -->
  <q-dialog v-model="popup" class="z-top">
    <q-card class="radius-16" style="width: 85%; max-width: 90vw">
      <q-bar dark class="text-white">
        <q-space />
        <q-btn dense flat round icon="close" color="white" v-close-popup />
      </q-bar>
      <q-card-section class="flex flex-center">
        <q-img
          src="https://techxero.com/assets/files/2021-09-23/1632436875-228477-pc-1024x579.jpg"
          style="max-width: 70vw"
          class="radius-16"
          spinner-color="primary"
          spinner-size="82px"
        />
      </q-card-section>

      <q-card-section>
        That PC is my main one acting as my everyday system. I do all my gaming
        on it. I have recently built it and all parts came from Amazon UK. It's
        an AMD Ryzen build. Click button below to check out build parts on PC
        Part Picker 😉
      </q-card-section>

      <q-card-section>
        At this point in time, this beast is running
        <span class="text-positive">Windows 11 Pro</span> /
        <span class="text-primary">XeroLinux Plasma</span> in Dual-Boot, until I
        decide otherwise.
      </q-card-section>

      <q-card-section class="text-center">
        <p class="text-negative">This build @ a glimpse</p>

        <p>ASUS ROG Swift PG279Q Monitor</p>
        <p>AsRock x570 Tai Chi | AMD Ryzen 5 3600x @ 3.8Ghz</p>
        <p>
          ROG STRiX GTX 1080 8Gb GDDR5X | TeamGroup Delta “R” 32GB DDR4 @3000Mhz
          RGB
        </p>
        <p>
          Corsair Obsidian 750D | Corsair RM750x (2018) | ROG Horus GK2000 RGB |
          Logi MX Ergo TrackBall
        </p>
        <p>
          Boot : 256gb SMG 960 Evo nVme | Profile Drive : 1TB SMG 860 Evo SATA |
          Games : 1TB SMG 970 Evo nVme
        </p>
      </q-card-section>

      <q-card-actions class="q-pa-md" align="right">
        <q-btn
          label="Learn more"
          color="accent"
          type="a"
          href="https://pcpartpicker.com/user/TechXero/saved/QCtmgs"
          target="_blank"
          v-close-popup
        />
      </q-card-actions>
    </q-card>
  </q-dialog>
</template>

<script>
import { useRoute } from "vue-router";
import { ref, computed } from "vue";

export default {
  setup() {
    const popup = ref(false);

    const home = () => {
      document.getElementById("hero").scrollIntoView({ behavior: "smooth" });
    };

    const about = () => {
      document.getElementById("about").scrollIntoView({ behavior: "smooth" });
    };

    const editions = () => {
      document
        .getElementById("download")
        .scrollIntoView({ behavior: "smooth" });
    };

    const xeroporn = () => {
      document
        .getElementById("xeroporn")
        .scrollIntoView({ behavior: "smooth" });
    };

    const route = useRoute();
    const isHome = computed(() => {
      return route.fullPath == "/";
    });

    return {
      about,
      editions,
      xeroporn,

      home,
      isHome,
      popup,
    };
  },
};
</script>
