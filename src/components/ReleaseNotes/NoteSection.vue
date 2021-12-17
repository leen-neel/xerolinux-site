<template>
  <div class="text-h4 text-bold">{{ title }}</div>
  <p class="q-mb-md">
    <slot></slot>
  </p>
</template>

<script>
export default {
  props: {
    title: String,
  },
};
</script>
