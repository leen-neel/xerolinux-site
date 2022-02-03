<template>
  <div
    id="about"
    :class="{
      'text-h2': $q.screen.gt.sm,
      'text-h4 text-bold': $q.screen.lt.md,
    }"
    class="q-mt-sm text-center q-pa-sm"
  >
    About XeroLinux
  </div>

  <div class="flex flex-center">
    <div
      class="text-justify q-pa-md q-mt-sm"
      :class="{
        'about-desc': $q.screen.gt.sm,
      }"
    >
      <p>
        This is XeroLinux - an Arch-based Distro, a personal project I am
        working on that I thought I would share, in case someone out there
        shares my passion for building Linux.
      </p>
      <p class="q-mt-lg">
        It Comes in 3 flavors, "Main Edition", "XFCE Edition" and "GNOME
        edition".
      </p>
      <div class="line-icon q-my-lg"></div>
      <p>
        So if you have a beast Rig and want to experience my vision to its
        fullest then you can't go wrong with the "Main Edition".
      </p>
      <p>
        If you have nVidia and want to benefit from Wayland, and you love GNOME,
        also you have a powerful enough config to run it, then this is the
        edition for you. Minimal tweaking for stability, and looks great.
      </p>
      <p>
        On the other hand, if performance is more important to you or your rig
        isn't powerful enough and you still want to give
        <storng>XeroLinux</storng> a try, then "XFCE Edition" is the answer for
        you.
      </p>
      <p class="q-mt-lg">As the saying goes...</p>
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
  </div>
</template>

<style lang="scss">
.about-desc {
  max-width: 97.5vw;
  background-color: #44475a;
  border-radius: 16px;
  margin-bottom: 10px;

  .q-card {
    background-color: #313341;
  }
}

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
