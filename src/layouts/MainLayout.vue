<template>
  <q-layout view="hHh lpR fff">
    <q-page-container>
      <NavBar v-if="$q.screen.gt.sm" />
      <NavBarMobile v-if="$q.screen.lt.md" />
      <router-view />

      <SiteFooter />
    </q-page-container>
  </q-layout>
</template>

<script>
import SiteFooter from "src/components/sections/SiteFooter.vue";
import NavBar from "src/components/sections/NavBar.vue";
import NavBarMobile from "src/components/sections/NavBarMobile.vue";
import { defineComponent } from "vue";

export default defineComponent({
  name: "MainLayout",
  components: {
    SiteFooter,
    NavBar,
    NavBarMobile,
  },
});
</script>
