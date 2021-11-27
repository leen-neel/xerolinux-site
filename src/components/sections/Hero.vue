<template>
  <div class="hero">
    <div class="absolute flex flex-center blur q-pa-lg column">
      <div class="text-h3 text-white text-center text-bold q-mb-md">
        XeroLinux
      </div>
      <q-btn class="btn" color="primary" icon="download" label="Download" />
    </div>
  </div>
</template>

<style lang="scss" scoped>
.hero {
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  background-image: url("/images/hero.jpg");
  height: 100vh;
}

.blur {
  height: 100vh;
  width: 100%;

  backdrop-filter: blur(7px);
}
</style>
