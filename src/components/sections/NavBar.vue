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
      label="Editions"
      flat
      style="font-size: 18px"
      @click="editions"
    />
    <q-btn
      v-if="isHome"
      label="XeroPorn"
      flat
      style="font-size: 18px"
      @click="xeroporn"
    />
    <q-btn
      v-if="isHome"
      label="Gallery"
      flat
      style="font-size: 18px"
      @click="gallery"
    />
    <q-btn
      label="Forum"
      flat
      style="font-size: 18px"
      type="a"
      href="https://forum.xerolinux.xyz/"
      target="_blank"
    />
  </div>
</template>

<script>
import { useRoute } from "vue-router";
import { computed } from "vue";
export default {
  setup() {
    const home = () => {
      document.getElementById("hero").scrollIntoView({ behavior: "smooth" });
    };

    const about = () => {
      document.getElementById("about").scrollIntoView({ behavior: "smooth" });
    };

    const editions = () => {
      document
        .getElementById("editions")
        .scrollIntoView({ behavior: "smooth" });
    };

    const xeroporn = () => {
      document
        .getElementById("xeroporn")
        .scrollIntoView({ behavior: "smooth" });
    };

    const gallery = () => {
      document.getElementById("gallery").scrollIntoView({ behavior: "smooth" });
    };

    const route = useRoute();
    const isHome = computed(() => {
      return route.fullPath == "/";
    });

    return {
      about,
      editions,
      xeroporn,
      gallery,
      home,
      isHome,
    };
  },
};
</script>
