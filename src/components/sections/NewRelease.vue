<template>
  <q-card
    v-if="hasNewRelease"
    class="
      bg-secondary
      text-white
      q-ma-md
      flex flex-center
      text-h4
      q-pa-lg
      radius-16
    "
  >
    New release on {{ date }}!
  </q-card>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  props: {
    date: String,
    hasNewRelease: Boolean,
  },
});
</script>
