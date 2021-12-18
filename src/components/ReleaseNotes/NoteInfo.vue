<template>
  <q-card class="info-card radius-16 bg-warning text-black">
    <q-card-section>
      <div class="text-h6 text-bold flex items-center">
        <q-icon v-if="icon" :name="icon" class="q-mr-sm" />
        {{ title }}
      </div>
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
    icon: String,
  },
};
</script>
