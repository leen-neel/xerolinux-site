<template>
  <q-badge
    v-if="hasAnnoouncement"
    color="negative"
    class="text-weight-bolder announcement-badge"
  >
    <slot name="badge"> </slot>
  </q-badge>
  <q-card
    v-if="hasAnnoouncement"
    class="bg-secondary text-white q-ma-md flex flex-center q-pa-sm radius-16"
    :class="{
      'announcement-title': $q.screen.gt.sm,
      'text-h6 text-bold': $q.screen.lt.md,
    }"
  >
    <slot> </slot>
  </q-card>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  props: {
    date: String,
    hasAnnoouncement: Boolean,
  },
});
</script>

<style lang="scss" scoped>
.announcement-title {
  font-size: 28px;
}
.announcement-badge {
  position: relative;
  bottom: -30px;
  right: -15px;
  z-index: 1;

  padding: 20px;
  border-radius: 32px;
  font-size: 15px;
}
</style>
