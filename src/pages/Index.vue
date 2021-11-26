<template>
  <q-page>
    <div class="hero">
      <div class="absolute flex flex-center blur q-pa-lg column">
        <div class="text-h3 text-white text-center text-bold q-mb-md">
          XeroLinux
        </div>
        <q-btn
          class="downloadBtn"
          color="primary"
          icon="download"
          label="Download"
        />
      </div>
    </div>
  </q-page>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "PageIndex",
});
</script>
