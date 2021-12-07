<template>
  <q-page>
    <NavBar v-if="$q.screen.gt.sm" />
    <NavBarMobile v-if="$q.screen.lt.md" />

    <Hero />

    <NewRelease date="06/12/2021" :hasNewRelease="true" />

    <About />

    <Editions />

    <XeroPorn />

    <Gallery />
  </q-page>
</template>

<script>
import About from "src/components/sections/About.vue";
import Editions from "src/components/sections/Editions.vue";
import Gallery from "src/components/sections/Gallery.vue";
import Hero from "src/components/sections/Hero.vue";
import NavBar from "src/components/sections/NavBar.vue";
import NavBarMobile from "src/components/sections/NavBarMobile.vue";
import NewRelease from "src/components/sections/NewRelease.vue";
import XeroPorn from "src/components/sections/XeroPorn.vue";

import { defineComponent } from "vue";

export default defineComponent({
  name: "PageIndex",
  components: {
    About,
    Hero,
    Editions,
    Gallery,
    NavBar,
    NavBarMobile,
    NewRelease,
    XeroPorn,
  },
});
</script>
