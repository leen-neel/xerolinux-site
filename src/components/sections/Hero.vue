<template>
  <div class="hero">
    <div class="absolute flex flex-center items-start blur q-pa-lg column">
      <img src="/images/logo.png" alt="" style="max-width: 300px" />

      <div class="text-h3 text-white text-center text-bold q-mb-md">
        XeroLinux
      </div>

      <p class="q-mt-md text-center" style="font-size: 15px">
        A Custom Arch-Based Distro With KDE by <strong>DarkXero.</strong>
      </p>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.hero {
  background-position: top;
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
