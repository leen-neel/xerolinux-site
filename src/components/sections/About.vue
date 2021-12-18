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

    <p class="q-mt-lg">
      It Comes in 2 flavors, "Main Edition" and "XFCE Edition". What's the
      difference between the two you may ask ? Let me explain.
    </p>

    <div class="q-mt-lg text-h4 header">- XeroLinux Main</div>
    <p class="q-mt-md">
      The former is our "Flagship" release, it uses <strong>KDE</strong> as its
      DE and offers a wide variety of packages to choose from during install,
      support for a wide host of Hardware, not to mention the level of
      customisation that KDE brings with it.
    </p>

    <div class="q-mt-lg text-h4 header">- XeroLinux XFCE</div>
    <p class="q-mt-md">
      While the latter was created for all of you out there that don't have
      powerful enough hardware to run our "Flagship" release that uses tons of
      effects and other tools that use a lot of system resources. It uses
      <strong>XFCE</strong> as its DE, as it's one of the lightest out there,
      that can still be made to look great without impacting performance. Don't
      worry though, it still retains most of the main features but with a bit
      less options.
    </p>

    <div class="line-icon q-my-lg"></div>

    <p>
      So if you have a beast Rig and want to experience my vision to its fullest
      then you can't go wrong with the "Main Edition".
    </p>

    <p class="q-mt-lg">
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
</template>

<style lang="scss">
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
