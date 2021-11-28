<template>
  <q-page>
    <NavBar v-if="$q.screen.gt.sm" />
    <NavBarMobile v-if="$q.screen.lt.md" />

    <Hero />

    <About />

    <Editions />

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
  },
});
</script>
