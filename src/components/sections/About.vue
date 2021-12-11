<template>
  <div id="about" class="text-h2 q-mt-sm text-center q-pa-sm">
    About XeroLinux
  </div>

  <div class="text-left q-pa-md q-mt-sm">
    <p>
      This is XeroLinux - an Arch-based Distro with KDE Plasma Desktop, a
      personal project I am working on that I thought I would share, in case
      someone out there shares my passion for building Linux.
    </p>

    <p>
      It Comes in 2 flavors, "Core Edition" and "Main Edition". What's the
      difference between the two you may ask ? Well "Core" is just Arch &
      Vanilla KDE with drivers install unlocked for you to select the right ones
      for your hardware whereas "Main" has all the bells an whistles, like a
      full custom rice complete with Latte-Dock and theme, to customized
      settings etc.
    </p>

    <div class="line-icon"></div>

    <p class="q-mt-sm">
      So if you just want to get started doing everything yourself, "Core" is
      for you, but if you want the ease of doing less and being up and running
      without much effort also you like the eye candy, then "Main" is the right
      choice.
    </p>

    <p>As the saying goes...</p>

    <q-card class="my-card">
      <q-card-section>
        <strong
          >"If you can't find the best Distro for you, then BUILD YOUR
          OWN!".</strong
        >
        That's the power of ArchLinux.
      </q-card-section>
    </q-card>
  </div>
</template>

<style lang="scss" scoped>
.line-icon {
  box-sizing: border-box;
  position: relative;
  text-align: center;
  background-image: url("/images/logoIcon.png");
  background-repeat: no-repeat;
  background-position: center;
  font-size: 0;
  height: 40px;
}
.line-icon::before,
.line-icon::after {
  box-sizing: border-box;
  width: 40%;
  height: 1px;
  border-top: 1px solid #d6d6d6;
  display: inline-block;
  content: "";
  margin-left: 5%;
  margin-right: 5%;
  position: relative;
  top: 50%;
  -moz-transform: translatey(-50%);
  -ms-transform: translatey(-50%);
  -o-transform: translatey(-50%);
  -webkit-transform: translatey(-50%);
  transform: translatey(-50%);
}
</style>
