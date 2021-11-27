<template>
  <q-page>
    <NavBar v-if="$q.screen.gt.sm" />
    <NavBarMobile id="compostable" v-if="$q.screen.lt.md" />

    <Hero />

    <About />

    <Editions />

    <Socials />
  </q-page>
</template>

<script>
import About from "src/components/sections/About.vue";
import Editions from "src/components/sections/Editions.vue";
import Hero from "src/components/sections/Hero.vue";
import NavBar from "src/components/sections/NavBar.vue";
import NavBarMobile from "src/components/sections/NavBarMobile.vue";
import Socials from "src/components/sections/Socials.vue";

import { defineComponent } from "vue";

export default defineComponent({
  name: "PageIndex",
  components: {
    About,
    Hero,
    Editions,
    Socials,
    NavBar,
    NavBarMobile,
  },
});
</script>
