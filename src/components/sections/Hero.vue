<template>
  <div class="hero">
    <div class="absolute flex flex-center items-start blur q-pa-lg column">
      <img src="/images/logo.png" alt="" style="max-width: 300px" />

      <div class="text-h3 text-white text-center text-bold q-mb-md">
        XeroLinux
      </div>

      <p class="q-mt-md text-center" style="font-size: 15px">
        A One Man's Vision of how It Could Be, Freedom of Choice
      </p>
    </div>

    <div class="row flex-center" style="position: relative; top: 82%">
      <q-btn
        color="white"
        icon="fab fa-telegram"
        flat
        round
        type="a"
        href="https://t.me/XeroLinux"
        target="_blank"
        size="20px"
      />
      <q-btn
        color="white"
        icon="fab fa-discord"
        flat
        round
        type="a"
        href="https://discord.gg/Xg6T78ahtK"
        target="_blank"
        size="20px"
      />
      <q-btn
        color="white"
        icon="fab fa-youtube"
        flat
        round
        type="a"
        href="https://youtube.com/c/XeroLinuxOfficial"
        target="_blank"
        size="20px"
      />
      <q-btn
        color="white"
        icon="fab fa-github"
        flat
        round
        type="a"
        href="https://github.com/XeroLinux"
        target="_blank"
        size="20px"
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
