<template>
  <q-page>
    <NoteHero topTitle="Release Notes" bottomTitle="XeroLinux Main" />

    <section class="q-pa-md q-mt-md">
      <note-section title="Title">
        Lorem ipsum dolor sit, amet consectetur adipisicing elit. Suscipit
        adipisci, recusandae sit placeat sapiente amet vero animi sunt
        voluptatum temporibus rem asperiores, quos harum impedit distinctio
        molestias libero necessitatibus consequatur.
      </note-section>

      <note-section title="Title">
        Lorem ipsum dolor sit, amet consectetur adipisicing elit. Suscipit
        adipisci, recusandae sit placeat sapiente amet vero animi sunt
        voluptatum temporibus rem asperiores, quos harum impedit distinctio
        molestias libero necessitatibus consequatur.
      </note-section>
    </section>
  </q-page>
</template>

<script>
import NoteHero from "src/components/ReleaseNotes/NoteHero.vue";
import NoteSection from "src/components/ReleaseNotes/NoteSection.vue";

export default {
  components: {
    NoteHero,
    NoteSection,
  },
};
</script>
