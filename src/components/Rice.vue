<template>
  <q-card class="radius-16 bg-dark text-white">
    <q-img
      :src="img"
      spinner-color="primary"
      spinner-size="82px"
      width="100%"
    />

    <q-card-section>
      <div class="text-center text-h3">{{ name }}</div>
    </q-card-section>

    <q-card-section class="q-pt-none">
      <div class="desc">
        <slot> </slot>
      </div>
    </q-card-section>

    <q-card-actions class="q-ma-sm" align="right">
      <q-btn
        type="a"
        target="_blank"
        :href="link"
        color="primary"
        class="q-pa-md"
        label="Installation guide"
      />
    </q-card-actions>
  </q-card>
</template>

<script>
import { defineComponent } from "vue";
export default defineComponent({
  name: "Rice",
  props: {
    name: String,
    description: String,
    link: String,
    img: String,
  },
});
</script>

<style lang="scss" scoped>
.desc {
  font-size: 15px;
}
</style>
