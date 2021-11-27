<template>
  <div class="text-h2 q-mt-sm text-center q-pa-sm">XeroLinux Editions</div>

  <div
    class="
      row
      flex-center
      q-gutter-md q-mt-sm
      col-xs-12 col-sm-6 col-md-4
      q-pa-sm
    "
  >
    <q-card class="edition-card">
      <q-img
        src="https://i.imgur.com/TNg4vJr.jpeg"
        spinner-color="primary"
        spinner-size="82px"
      />
      <q-card-section>
        <div class="text-h3">XeroLinux Main</div>
      </q-card-section>
      <q-card-section>
        This one is a bit long in the tooth to describe, suffice it to say that
        this one is where you get all the bells and whistles. It's got so many
        that you will HAVE to read the entire Release notes to get the big
        picture.
      </q-card-section>
    </q-card>

    <q-card class="edition-card">
      <q-img
        src="https://i.imgur.com/27KxEm6.jpeg"
        spinner-color="primary"
        spinner-size="82px"
      />
      <q-card-section>
        <div class="text-h3">XeroLinux Core</div>
      </q-card-section>
      <q-card-section>
        It’s a stripped down version of the main release. Yes, this will not
        have the fancy look that main edition has, nor does it have any of the
        bells n whistles. But it still retains the Driver selector page for best
        compatibility.
      </q-card-section>
    </q-card>
  </div>
</template>

<style lang="scss" scoped>
.edition-card {
  max-width: 600px;
}
</style>
