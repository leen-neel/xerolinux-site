<template>
  <div class="hero">
    <div class="absolute flex flex-center items-start blur q-pa-lg column">
      <img src="/images/logo.png" alt="" style="max-width: 300px" />

      <div class="text-h3 text-white text-center text-bold q-mb-md">
        XeroLinux
      </div>

      <div class="q-mt-sm text-center">
        An <strong>"Eyecandy"</strong> lover's wet dream.

        <br />

        A creation by <strong>DarkXero</strong>
      </div>
    </div>

    <q-card class="buttons-pos" style="background-color: transparent">
      <q-card-section class="text-center">
        ~ [You can find us on] ~
      </q-card-section>
      <q-card-actions align="center">
        <q-btn
          color="primary"
          icon="fab fa-telegram"
          round
          type="a"
          href="https://t.me/XeroLinux"
          target="_blank"
          size="15px"
          class="q-mx-sm"
        />
        <q-btn
          color="primary"
          icon="fab fa-discord"
          round
          type="a"
          href="https://discord.gg/Xg6T78ahtK"
          target="_blank"
          size="15px"
          class="q-mx-sm"
        />
        <q-btn
          color="primary"
          icon="fab fa-youtube"
          round
          type="a"
          href="https://youtube.com/c/XeroLinuxOfficial"
          target="_blank"
          size="15px"
          class="q-mx-sm"
        />
        <q-btn
          color="primary"
          icon="fab fa-github"
          round
          type="a"
          href="https://github.com/XeroLinux"
          target="_blank"
          size="15px"
          class="q-mx-sm"
        />
      </q-card-actions>
    </q-card>
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

.find-us {
  font-size: 21px;
}

.buttons-pos {
  position: relative;
  top: 82%;
  box-shadow: none;
}

@media (max-width: $breakpoint-xs-max) {
  .find-us {
    font-size: 20px;
  }

  .buttons-pos {
    top: 83%;
  }
}
</style>
