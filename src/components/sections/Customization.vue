<template>
  <div id="xeroporn"></div>
  <div class="text-h3 q-mt-xl text-center q-pa-sm">Customization</div>

  <div
    class="row flex-center q-gutter-md q-mt-sm col-xs-12 col-sm-6 col-md-4 q-pa-sm"
  >
    <Rices />
    <GrubThemes />
  </div>
</template>

<script>
import { defineComponent } from "vue";
import GrubThemes from "./GrubThemes.vue";
import Rices from "./Rices.vue";

export default defineComponent({
  components: {
    Rices,
    GrubThemes,
  },
});
</script>
