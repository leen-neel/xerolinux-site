<template>
  <q-card class="radius-16 bg-dark text-white">
    <q-img :src="img" spinner-color="primary" spinner-size="82px" width="100%">
      <q-btn
        icon="close"
        flat
        round
        dense
        v-close-popup
        class="absolute all-pointer-events"
        style="top: 8px; left: 92%"
      />
    </q-img>

    <q-card-section>
      <div class="text-center text-h3">{{ name }}</div>
    </q-card-section>

    <q-card-section class="q-pt-none">
      <div class="desc">
        <slot> </slot>
      </div>
    </q-card-section>

    <q-card-section class="q-pt-none">
      <div class="text-h6">Git Clone</div>
      <div class="desc syntax full-width q-pa-md q-mt-sm">
        <slot name="gc"> </slot>
      </div>
    </q-card-section>

    <q-card-section class="q-pt-none">
      <div class="text-h6">Set exec permission</div>
      <div class="desc syntax full-width q-pa-md q-mt-sm">
        sudo chmod +x ./install.sh
      </div>
    </q-card-section>

    <q-card-section class="q-pt-none">
      <div class="text-h6">Install theme</div>
      <div class="desc syntax full-width q-pa-md q-mt-sm">
        sudo ./install.sh
      </div>
    </q-card-section>
  </q-card>
</template>

<script>
import { defineComponent } from "vue";
export default defineComponent({
  name: "Rice",
  props: {
    name: String,
    img: String,
  },
});
</script>

<style lang="scss" scoped>
.desc {
  font-size: 15px;
}

.syntax {
  background-color: #282a36;
  border-radius: 8px;
}
</style>
