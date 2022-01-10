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
            <q-item-section> Customization </q-item-section>
          </q-item>

          <q-item
            v-if="isHome"
            @click="gallery"
            class="text-center q-ma-sm"
            clickable
          >
            <q-item-section> Gallery </q-item-section>
          </q-item>

          <q-item
            v-if="isHome"
            @click="popup = true"
            class="text-center q-ma-sm"
            clickable
            v-close-popup
          >
            <q-item-section> My PC Build </q-item-section>
          </q-item>

          <a href="https://forum.xerolinux.xyz/" target="_blank">
            <q-item class="text-center q-ma-sm" clickable v-close-popup>
              <q-item-section>
                <span class="no-padding">
                  Forum
                  <q-icon name="open_in_new" />
                </span>
              </q-item-section>
            </q-item>
          </a>
        </q-list>
      </q-menu>
    </q-btn>
  </div>

  <!-- PC Build -->
  <q-dialog v-model="popup" class="z-top">
    <q-card class="radius-16">
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

      <q-card-section class="row items-center">
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

      <q-card-actions class="q-pa-md" align="center">
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
import { defineComponent } from "vue";
import { useRoute } from "vue-router";
import { computed, ref } from "vue";
export default defineComponent({
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
      popup,
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
