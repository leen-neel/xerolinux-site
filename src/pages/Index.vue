<template>
  <q-page>
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
import Socials from "src/components/sections/Socials.vue";

import { defineComponent } from "vue";

export default defineComponent({
  name: "PageIndex",
  components: {
    About,
    Hero,
    Editions,
    Socials,
  },
});
</script>
