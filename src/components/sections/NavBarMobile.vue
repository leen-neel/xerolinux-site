<template>
  <div class="fixed-top row nav-bg full-width z-top q-pa-md q-gutter-sm">
    <div @click="home" class="cursor-pointer text-h4">XeroLinux</div>

    <q-space />
    <q-btn color="white" icon="menu" flat>
      <q-menu
        class="z-top"
        transition-show="jump-down"
        transition-hide="jump-up"
      >
        <q-list style="min-width: 100px">
          <q-item to="/" active-class="" class="text-center q-ma-sm" clickable>
            <q-item-section> Home </q-item-section>
          </q-item>

          <q-item
            v-if="isHome"
            @click="about"
            class="text-center q-ma-sm"
            clickable
          >
            <q-item-section> About </q-item-section>
          </q-item>

          <q-item
            v-if="isHome"
            @click="editions"
            class="text-center q-ma-sm"
            clickable
          >
            <q-item-section> Download </q-item-section>
          </q-item>

          <q-item
            v-if="isHome"
            @click="xeroporn"
            class="text-center q-ma-sm"
            clickable
          >
            <q-item-section> XeroPorn </q-item-section>
          </q-item>

          <q-item
            v-if="isHome"
            @click="gallery"
            class="text-center q-ma-sm"
            clickable
          >
            <q-item-section> Gallery </q-item-section>
          </q-item>

          <a href="https://forum.xerolinux.xyz/" target="_blank">
            <q-item class="text-center q-ma-sm" clickable v-close-popup>
              <q-item-section> Forum </q-item-section>
            </q-item>
          </a>
        </q-list>
      </q-menu>
    </q-btn>
  </div>
</template>

<script>
import { defineComponent } from "vue";
import { useRoute } from "vue-router";
import { computed } from "vue";
export default defineComponent({
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
});
</script>

<style lang="scss" scoped>
a {
  text-decoration: none;
}
</style>
