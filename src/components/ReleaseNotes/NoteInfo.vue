<template>
  <q-card class="info-card bg-warning text-black">
    <q-card-section>
      <div class="text-h6 text-bold">{{ title }}</div>
    </q-card-section>
    <q-card-section>
      <slot> </slot>
    </q-card-section>
  </q-card>
</template>

<script>
export default {
  props: {
    title: String,
  },
};
</script>
