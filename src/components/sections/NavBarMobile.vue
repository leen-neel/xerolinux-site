<template>
  <div class="absolute-top row z-top q-ma-md q-gutter-sm">
    <img src="/images/logo.png" alt="Xerolinux" style="max-width: 50px" />

    <q-space />

    <q-btn color="white" icon="menu" flat :persistent="false">
      <q-menu fit transition-show="jump-down" transition-hide="jump-up">
        <q-list style="min-width: 100px">
          <q-item clickable v-close-popup>
            <q-item-section>
              <q-btn
                label="About"
                flat
                style="font-size: 18px"
                type="a"
                href="#about"
              />
            </q-item-section>
          </q-item>

          <q-item clickable v-close-popup>
            <q-item-section>
              <q-btn
                label="Editions"
                flat
                style="font-size: 18px"
                type="a"
                href="#editions"
              />
            </q-item-section>
          </q-item>

          <q-item clickable v-close-popup>
            <q-item-section type="a" href="google.com">
              <q-btn
                label="Socials"
                flat
                style="font-size: 18px"
                type="a"
                href="#socials"
              />
            </q-item-section>
          </q-item>
        </q-list>
      </q-menu>
    </q-btn>
  </div>
</template>
