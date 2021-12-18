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
      rgba(255, 255, 255, 0.13) 0%,
      rgba(40, 42, 54, 0.13) 50.37%,
      rgba(40, 42, 54, 0.92) 87.55%
    ),
    url("/images/hero.jpg") no-repeat center / cover;
  height: 50vh;
}
</style>
