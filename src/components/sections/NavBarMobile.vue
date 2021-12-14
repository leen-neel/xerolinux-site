<template>
  <div class="fixed-top row nav-bg full-width z-top q-pa-md q-gutter-sm">
    <div class="text-h4">XeroLinux</div>

    <q-space />

    <q-btn color="white" icon="menu" flat>
      <q-menu
        class="z-top"
        transition-show="jump-down"
        transition-hide="jump-up"
      >
        <q-list style="min-width: 100px">
          <q-item @click="about" class="text-center q-ma-sm" clickable>
            <q-item-section> About </q-item-section>
          </q-item>

          <q-item @click="editions" class="text-center q-ma-sm" clickable>
            <q-item-section> Editions </q-item-section>
          </q-item>

          <q-item @click="xeroporn" class="text-center q-ma-sm" clickable>
            <q-item-section> XeroPorn </q-item-section>
          </q-item>

          <q-item @click="gallery" class="text-center q-ma-sm" clickable>
            <q-item-section> Gallery </q-item-section>
          </q-item>

          <a href="https://forum.xerolinux.xyz/">
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
import { defineComponent, ref } from "vue";

export default defineComponent({
  setup() {
    const menu = ref(true);

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
    return {
      menu,
      about,
      editions,
      xeroporn,
      gallery,
    };
  },
});
</script>

<style lang="scss" scoped>
a {
  text-decoration: none;
}
</style>
