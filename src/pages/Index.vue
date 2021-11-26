<template>
  <q-page>
    <Hero />

    <About />
  </q-page>
</template>

<script>
import About from "src/components/sections/About.vue";
import Hero from "src/components/sections/Hero.vue";
import { defineComponent } from "vue";

export default defineComponent({
  name: "PageIndex",
  components: {
    About,
    Hero,
  },
});
</script>
