<template>
  <q-page>
    <NoteHero topTitle="Release Notes" bottomTitle="XeroLinux XFCE" />

    <section class="q-pa-md q-mt-md">
      <note-section title="Hey there XeroLinux users!">
        Another month, anther release. Now, hold your horses, this is by no
        means a Major release, it's just a bugfix one. But I have fixed so many
        bugs I felt it deserved its own new Rice (more on that later on). I know
        I said no more releases, but, I felt that this one needed its own post
        to talk about all the bugs I have squashed.
      </note-section>

      <div class="text-center q-mb-sm text-h4">⚠️ Disclaimer ⚠️</div>

      <note-info icon="help_outline" class="q-mb-lg bg-warning" title="Note">
        <p>
          <strong>XeroLinux</strong> was born as a <strong>KDE</strong> only
          minimal Distro. It has now grown to include <strong>XFCE</strong>. And
          no <strong>WMs</strong> please do not request any. The more I add the
          further it will drift from original vision.
        </p>

        <p>
          For this reason, please do not ask me to add any. I am not saying this
          to be negative. Look at it from my perspective, I am a one man show, I
          cannot bite off more than I can chew. How can I support something I
          have no idea about ? I am just being transparent with y'all..
        </p>
      </note-info>

      <div class="text-center q-mb-sm text-h4">What is XFCE edition?</div>

      <note-info icon="help_outline" class="q-mb-lg bg-warning" title="Note">
        <p>
          It was created for all of you out there that don't have powerful
          enough hardware to run our "Flagship" release that uses tons of
          effects and other tools that use a lot of system resources. It uses
          XFCE as its DE, as it's one of the lightest out there, that can still
          be made to look great without impacting performance. Don't worry
          though, it still retains most of the main features but with a bit less
          options.
        </p>
      </note-info>

      <div class="flex q-mb-lg flex-center">
        <img class="radius-16" src="https://i.imgur.com/jnEy01P.png" />
      </div>

      <div class="text-left q-mb-lg text-h4">
        Kindly read entire Article before installing
      </div>

      <div class="text-h6 text-left text-bold">System Requirements:</div>
      <ul class="q-mb-lg">
        <li>
          <strong>Minimum:</strong> Core i3 or AMD Equivalent CPU, 2gb RAM,
          Intel integrated Graphics, and 16gb Storage.
        </li>
        <li>
          <strong>Recommended:</strong> Core i7 or AMD Equivalent CPU, 16gb RAM,
          AMD/900 series <strong>nVidia GPU</strong>, and 32gb Storage.
        </li>
      </ul>

      <div class="text-h6 text-left text-bold">How to Burn ISO to USB:</div>
      <p class="q-mb-lg">
        The recommended method to create USB is to use
        <a href="https://www.balena.io/etcher/" target="_blank">Etcher</a> or
        <a
          target="_blank"
          href="https://forum.xerolinux.xyz/showthread.php?tid=30"
          >Ventoy</a
        >. Do not use Rufus. For better results it's better to use one of those
        two. Rufus is for Windows.
      </p>

      <div class="text-h6 q-mb-sm text-left text-bold">AUR Helper:</div>
      <note-info icon="help_outline" class="q-mb-lg bg-warning" title="Note">
        <p>
          <strong>XeroLinux</strong> uses <strong>Paru</strong> as the
          <strong>AUR</strong> helper instead of <strong>YaY</strong>.. Just use
          pget packagename in Terminal to grab AUR stuff... If you prefer YaY
          then get it with Paru lol...
        </p>
      </note-info>

      <div class="text-h6 q-mb-sm text-left text-bold">New Calamares:</div>
      <p>
        Calamares installer has been updated to v3.2.49.1. It fixed many issues,
        among which are the following :
      </p>
      <ul class="q-mb-lg">
        <li>
          The option to send logs when an installation failed is now working
          again.
        </li>
        <li>
          <strong>Calamares</strong> can now display
          <strong>Pacman</strong> actions under the progress bar.
        </li>
        <li>Fixes in the partition, zfs and packages modules.</li>
      </ul>

      <div class="text-h6 q-mb-sm text-left text-bold">"nVidia" On Boot:</div>

      <div class="flex q-mb-lg flex-center">
        <img class="radius-16" src="https://i.imgur.com/qXowiDl.png" />
      </div>
      <p>
        The other issue was the one where nVidia drivers would get you stuck on
        a black screen or won't allow you to get to the installer. So added the
        right boot options to help with that. Just make sure to select the right
        one for you. For example if you have an nVidia card select one of the
        two nVidia options.
      </p>

      <note-section title="The Xero XFCE Rice">
        <p>
          Well, when it comes to ricing, that's where
          <strong>XeroLinux</strong> shines right ? For top panel we opted to
          use
          <a href="https://polybar.github.io/" target="_blank">PolyBar</a> with
          the
          <a
            href="https://github.com/adi1090x/polybar-themes#cuts"
            target="_blank"
            >Cuts</a
          >
          theme. As for the Dock, we opted to use
          <a href="https://github.com/ricotz/plank" target="_blank">Plank</a>,
          suitable for XFCE and lightweight.
        </p>
        <p class="q-mb-lg">
          Finally we used a various assortment of lightweight tweaks and effects
          to give it an oompf... Without making it eat up more resources than it
          should.
        </p>
      </note-section>

      <div class="text-h6 q-mb-sm text-left text-bold">
        Other Various features :
      </div>
      <div class="flex flex-center">
        <q-video
          class="q-mb-sm radius-16"
          src="https://www.youtube.com/embed/w1XYnBtHVZE?rel=0"
        />
      </div>
      <ul>
        <li>
          <strong>OS prober</strong> is installed by default for managing
          multi-booting systems.
        </li>
        <li>
          <strong>VMD</strong> support been added to enable
          <strong>Intel RST Drives</strong> to berecognized.
        </li>
        <li>
          Uses <strong>ZSTD</strong> compression for faster compiling. (Credit
          to <strong>ArcoLinux</strong>)
        </li>
        <li>
          Supports more <strong>PCIe-based M.2</strong> drives on ISO boot and
          to <strong>GRUB</strong>.
        </li>
      </ul>
    </section>
  </q-page>
</template>

<script>
import NoteHero from "src/components/ReleaseNotes/NoteHero.vue";
import NoteSection from "src/components/ReleaseNotes/NoteSection.vue";
import NoteInfo from "src/components/ReleaseNotes/NoteInfo.vue";

export default {
  components: {
    NoteHero,
    NoteSection,
    NoteInfo,
  },
};
</script>

<style lang="scss">
.q-video {
  width: 700px;
  height: 350px;
}

@media (max-width: $breakpoint-xs-max) {
  .q-video {
    width: 100%;
    height: auto;
  }
}
</style>
