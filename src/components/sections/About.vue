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

    <q-video
      style="border-radius: 16px"
      src="https://www.youtube.com/embed/UKg43SFtAL8"
      :ratio="16 / 9"
    />

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
