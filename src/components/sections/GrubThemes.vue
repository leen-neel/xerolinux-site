<template>
  <q-card class="grub-card radius-16">
    <q-img
      src="https://i.imgur.com/DWDNOv1.jpeg"
      spinner-color="primary"
      spinner-size="82px"
      height="380px"
    />

    <q-card-section>
      <div class="text-h3 text-center header">Grub Themes</div>
    </q-card-section>

    <q-card-actions vertical align="center">
      <q-btn
        label="XeroNord"
        color="accent"
        class="btn q-ma-sm"
        @click="xeronord = true"
        target="_blank"
      />

      <div class="row">
        <q-btn
          label="Star Wars"
          color="accent"
          class="btn q-ma-sm"
          target="_blank"
          @click="starwars = true"
        />
        <q-btn
          label="Draft Punk"
          color="accent"
          class="btn q-ma-sm"
          target="_blank"
          @click="draftpunk = true"
        />
        <q-btn
          label="T-R-O-N"
          color="accent"
          class="btn q-ma-sm"
          target="_blank"
          @click="tron = true"
        />
        <q-btn
          label="XeroComp"
          color="accent"
          class="btn q-ma-sm"
          target="_blank"
          @click="xcomp = true"
        />
      </div>
    </q-card-actions>
  </q-card>

  <!-- XeroNord -->
  <q-dialog
    v-model="xeronord"
    transition-show="slide-up"
    transition-hide="slide-down"
    class="z-top"
  >
    <Grub name="XeroNord" img="https://i.imgur.com/DWDNOv1.jpeg">
      This is where <strong>XeroNord</strong> Grub Theme will be. Constantly
      updated so keep coming back. I included a script that makes installing
      much easier, just follow steps below :

      <template v-slot:gc>
        git clone https://github.com/TechXero/XeroNord-Grub.git
      </template>
    </Grub>
  </q-dialog>

  <!-- Star wars -->
  <q-dialog
    v-model="starwars"
    transition-show="slide-up"
    transition-hide="slide-down"
    class="z-top"
  >
    <Grub name="Star Wars" img="https://i.imgur.com/fj4jPJf.png">
      This is where <strong>Star Wars: The Last Jedi</strong> inspired Grub
      Theme will be. Constantly updated so keep coming back. I included a script
      that makes installing much easier, just follow steps below :

      <template v-slot:gc>
        git clone https://github.com/TechXero/StarWarsGrub.git
      </template>
    </Grub>
  </q-dialog>

  <!-- Draft punk -->
  <q-dialog
    v-model="draftpunk"
    transition-show="slide-up"
    transition-hide="slide-down"
    class="z-top"
  >
    <Grub name="Draft Punk" img="https://i.imgur.com/kOHZXLe.png">
      This is where <strong>Daft Punk</strong> inspired Grub Theme will be.
      Constantly updated so keep coming back. I included a script that makes
      installing much easier, just follow steps below :

      <template v-slot:gc>
        git clone https://github.com/TechXero/DaftGrub.git
      </template>
    </Grub>
  </q-dialog>

  <!-- Tron -->
  <q-dialog
    v-model="tron"
    transition-show="slide-up"
    transition-hide="slide-down"
    class="z-top"
  >
    <Grub name="T-R-O-N" img="https://i.imgur.com/zhxPdqw.png">
      This is where <strong>TRON: Legacy</strong> inspired Grub Theme will be.
      Constantly updated so keep coming back. I included a script that makes
      installing much easier, just follow steps below :

      <template v-slot:gc>
        git clone https://github.com/TechXero/TronGrub.git
      </template>
    </Grub>
  </q-dialog>

  <!-- XCoomp -->
  <q-dialog
    v-model="xcomp"
    transition-show="slide-up"
    transition-hide="slide-down"
    class="z-top"
  >
    <Grub
      name=" Xero-Compromise"
      img="https://imghost.techxero.com/images/ovB.png"
    >
      This is where <strong>Xero-Compromise</strong> Grub Theme will be.
      Constantly updated so keep coming back. I included a script that makes
      installing much easier, just follow steps below :
      <template v-slot:gc>
        git clone https://github.com/TechXero/XeroComp.git
      </template>
    </Grub>
  </q-dialog>
</template>

<script>
import { defineComponent, ref } from "vue";
import Grub from "../Grub.vue";

export default defineComponent({
  name: "GrubThemes",
  components: {
    Grub,
  },
  setup() {
    return {
      xeronord: ref(false),
      starwars: ref(false),
      draftpunk: ref(false),
      tron: ref(false),
      xcomp: ref(false),
    };
  },
});
</script>

<style lang="scss" scoped>
.grub-card {
  width: 600px;
}
.btn {
  font-size: 13px;
}

@media (max-width: $breakpoint-xs-max) {
  .btn {
    font-size: 10px;
  }
}
</style>
