<template>
  <q-page>
    <NoteHero topTitle="Release Notes" bottomTitle="XeroLinux Main" />

    <section class="q-pa-md q-mt-md">
      <note-section title="Hey there XeroLinux users!">
        Another month, anther release. Now, hold your horses, this is by no
        means a Major release, it's just a bugfix one. But I have fixed so many
        bugs I felt it deserved its own new Rice (more on that later on). I know
        I said no more releases, but, I felt that this one needed its own post
        to talk about all the bugs I have squashed.
      </note-section>

      <div class="text-center q-mb-sm text-h4">⚠️ Disclaimer ⚠️</div>

      <note-info class="q-mb-lg" title="Note">
        <p>
          XeroLinux was born as a KDE only minimal Distro. It has now grown to
          include XFCE. And no WMs please do not request any. The more I add the
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

      <note-info class="q-mb-lg" title="Note">
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
      <ul>
        <li>
          <strong>Minimum:</strong> Core i3 or AMD Equivalent CPU, 2gb RAM,
          Intel integrated Graphics, and 16gb Storage.
        </li>
        <li>
          <strong>Recommended:</strong> Core i7 or AMD Equivalent CPU, 16gb RAM,
          AMD/900 series <strong>nVidia GPU</strong>, and 32gb Storage.
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
