<template>
  <div class="absolute-top row z-top q-ma-md q-gutter-sm">
    <div class="text-h4">XeroLinux</div>

    <q-space />

    <q-btn color="white" icon="menu" flat>
      <q-menu transition-show="jump-down" transition-hide="jump-up">
        <q-list style="min-width: 100px">
          <a href="#about">
            <q-item class="text-center q-ma-sm" clickable v-close-popup>
              <q-item-section> About </q-item-section>
            </q-item>
          </a>

          <a href="#editions">
            <q-item class="text-center q-ma-sm" clickable v-close-popup>
              <q-item-section> Editions </q-item-section>
            </q-item>
          </a>

          <a href="#gallery">
            <q-item class="text-center q-ma-sm" clickable v-close-popup>
              <q-item-section> Gallery </q-item-section>
            </q-item>
          </a>
        </q-list>
      </q-menu>
    </q-btn>
  </div>
</template>

<script>
import { defineComponent, ref } from "vue";

export default defineComponent({
  setup() {
    const menu = ref(true);
    return {
      menu,
    };
  },
});
</script>

<style lang="scss" scoped>
a {
  text-decoration: none;
}
</style>
