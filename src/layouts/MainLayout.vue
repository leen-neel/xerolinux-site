<template>
  <q-layout view="hHh lpR fff">
    <q-page-container>
      <router-view />

      <SiteFooter />
    </q-page-container>
  </q-layout>
</template>

<script>
import SiteFooter from "src/components/sections/SiteFooter.vue";
import { defineComponent } from "vue";

export default defineComponent({
  name: "MainLayout",
  components: {
    SiteFooter,
  },
});
</script>
