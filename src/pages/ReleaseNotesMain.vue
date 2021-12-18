<template>
  <NoteHero topTitle="Release Notes" bottomTitle="XeroLinux Main" />

  <section class="q-pa-md q-mt-md">
    <note-section title="Hey there XeroLinux users!">
      Another month, anther release. Now, hold your horses, this is by no means
      a Major release, it's just a bugfix one. But I have fixed so many bugs I
      felt it deserved its own new Rice (more on that later on). I know I said
      no more releases, but, I felt that this one needed its own post to talk
      about all the bugs I have squashed.
    </note-section>

    <div class="text-center q-mb-sm text-h4">⚠️ Disclaimer ⚠️</div>

    <note-info
      icon="help_outline"
      class="q-mb-lg bg-positive bg-positive"
      title="Note"
    >
      <p>
        <strong>XeroLinux</strong> was born as a <strong>KDE</strong> only
        minimal Distro. It has now grown to include <strong>XFCE</strong>. And
        no <strong>WMs</strong> please do not request any. The more I add the
        further it will drift from original vision.
      </p>

      <p>
        For this reason, please do not ask me to add any. I am not saying this
        to be negative. Look at it from my perspective, I am a one man show, I
        cannot bite off more than I can chew. How can I support something I have
        no idea about ? I am just being transparent with y'all..
      </p>
    </note-info>

    <div class="text-center q-mb-sm text-h4">What is Main edition?</div>

    <note-info icon="help_outline" class="q-mb-lg bg-positive" title="Note">
      <p>
        This one is a bit long in the tooth to describe, suffice it to say that
        this one is where you get all the bells and whistles. It's got so many
        that you will HAVE to read the entire Release notes to get the big
        picture.
      </p>
    </note-info>

    <div class="flex flex-center">
      <q-video
        class="q-mb-sm radius-16"
        src="https://www.youtube.com/embed/UKg43SFtAL8?rel=0"
      />
    </div>

    <note-info icon="help_outline" class="q-mb-lg bg-positive" title="Note">
      <p>
        It uses new Rice, got Snapper n TimeShift as well as my new XeroLinux
        Tool with which you can do some of the post install stuff and much much
        much more...
      </p>
    </note-info>

    <div class="text-left q-mb-lg text-h4">
      Kindly read entire Article before installing
    </div>

    <div class="text-h6 text-left text-bold">System Requirements:</div>
    <ul class="q-mb-lg">
      <li>
        <strong>Minimum:</strong> Core i5 or AMD Equivalent CPU, 8gb RAM, Intel
        XE Graphics, and 16gb Storage.
      </li>
      <li>
        <strong>Recommended:</strong> Core i7 or AMD Equivalent CPU, 16gb RAM,
        AMD/900 series nVidia GPU, and 32gb Storage.
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
    <note-info icon="help_outline" class="q-mb-lg bg-positive" title="Note">
      <p>
        <strong>XeroLinux</strong> uses <strong>Paru</strong> as the
        <strong>AUR</strong> helper instead of <strong>YaY</strong>.. Just use
        pget packagename in Terminal to grab AUR stuff... If you prefer YaY then
        get it with Paru lol...
      </p>
    </note-info>

    <div class="text-h6 q-mb-sm text-left text-bold">Before installing:</div>
    <p class="q-mb-lg">
      Keep in mind that not everything in Calamares is meant to be installed.
      Selecting everything will result in many conflicts and longer install
      time. Only select what you need and make sure to only install correct
      drivers for your hardware including Audio... Also do not forget to check
      This Article I wrote about a few of the included Terminal Aliases... For
      full list just type alias in terminal to see them all...
    </p>

    <div class="text-h6 q-mb-sm text-left text-bold">New Calamares:</div>
    <ul>
      <li>fstrim.tim is now enabled by default.</li>
      <li>
        The option to send logs when an installation failed is now working
        again.
      </li>
      <li>
        <strong>Calamares</strong> can now display
        <strong>Pacman</strong> actions under the progress bar.
      </li>
      <li>
        <strong>BTRFS</strong> now uses zstd for installation on both SSD and
        HDD.
      </li>
      <li>
        New <strong>XFS</strong> partition scheme added to
        <strong>Calamares</strong> if you need it.
      </li>
      <li>
        fixes in the partition, <strong>zfs</strong> and packages modules.
      </li>
    </ul>
    <p class="q-mb-lg">
      Finally I have dome more packages, removed others, mainly nVidia drivers,
      since they are now on the ISO itself. (Pascal cards and newer only...).
      Also reorganized the Packages a bit so you have a better idea what they
      are.
    </p>

    <div class="text-h6 q-mb-sm text-left text-bold">"nVidia" On Boot:</div>
    <div class="flex q-mb-lg flex-center">
      <img class="radius-16" src="https://i.imgur.com/qXowiDl.png" />
    </div>
    <p class="q-mb-lg">
      The other issue was the one where nVidia drivers would get you stuck on a
      black screen or won't allow you to get to the installer. So added the
      right boot options to help with that. Just make sure to select the right
      one for you. For example if you have an nVidia card select one of the two
      nVidia options. More info on
      <a href="https://forum.xerolinux.xyz/thread-7.html">this forum thread.</a>
    </p>

    <div class="text-h6 q-mb-sm text-left text-bold">KDE Wayland Session:</div>
    <div class="flex q-mb-lg flex-center">
      <img class="radius-16" src="https://i.imgur.com/uUQL5YS.png" />
    </div>
    <p>
      I have finally added
      <a href="https://community.kde.org/KWin/Wayland" target="_blank"
        >KDE Wayland</a
      >
      Session to ISO, enabling you to use it. But it's not all roses, yet.
      Especially if you are an <strong>nVidia</strong> owner like I am. Yes, if
      you are, then you are either out of luck, since
      <strong>nVidia</strong> did not yet bake the required modules into the
      driver yet, so you will have to do some tinkering to get it to work. If
      you do not feel comfortable or confident enough to do it then just use
      <strong>Xorg (X11)</strong> to log in and skip
      <strong>Wayland</strong> for now...
    </p>

    <note-info icon="help_outline" class="q-mb-lg bg-positive" title="Note">
      <p>
        Kindly note, that I will not be providing support in that area since, I
        am not yet confident in using it. But feel free to visit any of the
        links provided below for more information and troubleshooting...
      </p>
    </note-info>

    <ul>
      <li>
        <a
          href="https://community.kde.org/Plasma/Wayland/Nvidia"
          target="_blank"
          >KDE Wayland/nVidia</a
        >
      </li>
      <li>
        <a
          href="https://discovery.endeavouros.com/nvidia/nvidia-optional-enhancements-and-troubleshooting/2021/03/"
          target="_blank"
          >nVidiaOptiona Enhancements and Troubleshooting</a
        >
      </li>
    </ul>

    <note-info icon="help_outline" class="q-mb-lg bg-positive" title="Note">
      <p>
        If I were you I would stick to <strong>X11</strong> for now. I just
        added <strong>Wayland</strong> for the future when
        <strong>nVidia</strong> decides to bake it into their drivers. But it's
        up to you, I have provided the links, best of luck...
      </p>
    </note-info>

    <div class="text-h6 q-mb-sm text-left text-bold">
      New Revamped Config Tool:
    </div>
    <p>
      This release has seen many optimizations, among which the Configuration
      tool. I decided to work my butt off making it slimmer, and rework the
      options available.
    </p>
    <div class="flex q-mb-lg flex-center">
      <img class="radius-16" src="https://i.imgur.com/7CGR9BO.png" />
    </div>
    <p>
      It went on a sort of a design diet, lol. Now it's sleeker looking. I have
      moved some options around, added a few and removed others. It will keep
      evolving with every update. So picture above might be different to what
      options it now has. But you get the idea 😉
    </p>

    <div class="text-h6 q-mb-sm text-left text-bold">Refreshed rice:</div>
    <div class="flex q-mb-lg flex-center">
      <img
        class="radius-16"
        src="https://cdn.discordapp.com/attachments/912888928749645896/917800804096806942/New.jpg"
      />
    </div>
    <p>
      Well, when it comes to ricing, that's where
      <strong>XeroLinux</strong> shines right ? For top panel as well as Dock we
      are using
      <a href="https://github.com/KDE/latte-dock" target="_blank">Latte-Dock</a
      >. A bit heavy on resources, I would agree, but nothing comes close to its
      level of customization. We also use the famous
      <a href="https://github.com/xerolinux/xero-layan-git" target="_blank"
        >Layan</a
      >
      theme, with the
      <a
        href="https://github.com/vinceliuice/Tela-circle-icon-theme"
        target="_blank"
        >Tela Circle icons</a
      >. Those go so well together it's not funny.
    </p>
    <p>
      We also applied a ton of KWin and Desktop Effects, which are also taxing
      on resources, that's the reason for which this edition was not intended
      for old systems lacking in the specs department. This is the Flagship,
      which is why we did not spare any expense to make it look awesome !
    </p>
    <div class="flex q-mb-lg flex-center">
      <img class="radius-16" src="https://i.imgur.com/eEpE5rs.jpg" />
    </div>
    <p>
      Don't worry though, there will be new stand-alone rices in the future, I
      will not stop. It's just that, some users have voiced their confusion and
      I have listened. Anyway there ya go 😉
    </p>

    <div class="text-h6 q-mb-sm text-left text-bold">Audio Drivers:</div>
    <p>
      I gave you, the user, freedom of choice even in the Audio Driver
      department. In case you were living under a rock or something, there
      basically 2 Audio Driver Systems, <strong>PulseAudio</strong> and
      <strong>PipeWire</strong>. Pulse is aging, being more suitable for legacy
      hardware, whereas Pipe is quickly becoming the go to standard with support
      for modern hardware.
    </p>

    <div class="flex flex-center">
      <q-video
        class="q-mb-sm radius-16"
        src="https://www.youtube.com/embed/HxEXMHcwtlI?rel=0"
      />
    </div>

    <p class="q-mb-lg">
      I give you the choice between the 2. So please make sure to only select
      one of them and not bot during installation to avoid conflicts.
    </p>

    <div class="text-h6 q-mb-sm text-left text-bold">
      Game Launchers Removed:
    </div>
    <p>
      I took the hard decision to remove Game Launchers from the installer,
      simply because it caused some issues for a few users. Gaming on Linux is
      getting better with time, but installing the tools not straightforward. I
      do understand that some other distros out there provide them, but have you
      noticed that most do it After install and not During ? That's because they
      require manual work for them to work correctly.
    </p>
    <p class="q-mb-lg">
      Don't worry though, I have written an article about an awesome tool that
      will get you up and gaming in no time at all. It's called
      <strong>LibreGaming</strong>. Hit
      <a
        href="https://forum.xerolinux.xyz/showthread.php?tid=15"
        target="_blank"
        >that article</a
      >
      and get your game on!
    </p>

    <div class="text-h6 q-mb-sm text-left text-bold">Other Various fixes:</div>
    <div class="flex flex-center">
      <q-video
        :ratio="16 / 9"
        src="https://www.youtube.com/embed/w1XYnBtHVZE?rel=0"
      />
    </div>
    <ul>
      <li>Fixed reset script which allows you to get back to stock config.</li>

      <li>
        <strong>OS prober</strong> is installed by default for managing
        multi-booting systems.
      </li>
      <li>
        <strong>VMD</strong> support been added to enable
        <strong>Intel RST Drives</strong> to berecognized.
      </li>
      <li>
        Switched to <strong>ZSTD</strong> compression for faster compiling.
        (Credit to <strong>ArcoLinux</strong>)
      </li>
      <li>
        Supports more <strong>PCIe-based M.2</strong> drives on ISO boot and to
        <strong>GRUB</strong>.
      </li>
      <li>
        Fixed issue with <strong>Snaps</strong> not launching after install due
        to missing <strong>$PATH</strong> variable.
      </li>
    </ul>
  </section>
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
