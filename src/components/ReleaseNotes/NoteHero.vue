<template>
  <section class="hero flex flex-center">
    <div class="text-center column">
      <div class="text-h2 no-margin">{{ topTitle }}</div>
      <div class="text-h4">{{ bottomTitle }}</div>
    </div>
  </section>
</template>

<script>
export default {
  props: {
    topTitle: String,
    bottomTitle: String,
  },
};
</script>

<style lang="scss" scoped>
.hero {
  background: linear-gradient(
    180deg,
    rgba(40, 42, 54, 0.065) 30.88%,
    rgba(0, 0, 0, 0.5) 67.29%
  );
  background: url("/images/hero.jpg") no-repeat center / cover;
  height: 50vh;
}
</style>
