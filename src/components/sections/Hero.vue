<template>
  <div class="hero">
    <div class="absolute flex flex-center items-start blur q-pa-lg column">
      <div class="text-h3 text-white text-center text-bold q-mb-md">
        XeroLinux
      </div>

      <p class="q-mt-md text-center" style="font-size: 15px">
        Welcome to XeroLiniux's official page!
      </p>

      <p class="q-mb-md text-center" style="font-size: 15px">
        Feel free to look around and learn more about the distro.
      </p>

      <q-btn
        class="btn"
        color="primary"
        icon="arrow_downward"
        label="Editions"
        type="a"
        href="#about"
      />
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
