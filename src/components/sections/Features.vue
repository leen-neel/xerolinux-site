<template>
  <section class="q-my-md">
    <div
      class="q-gutter-md flex flex-center"
      :class="{
        row: $q.screen.gt.sm,
        column: $q.screen.lt.md,
      }"
    >
      <!-- Feature 1 -->
      <div class="column feature">
        <div class="flex flex-center">
          <q-icon color="primary" name="language" size="55px" />
        </div>
        <div class="text-h6 text-bold">This is XeroLinux</div>
        <p>A fully featured Custom Arch-Based Distro by DarkXero</p>
      </div>

      <div class="column feature">
        <div class="flex flex-center">
          <q-icon color="negative" name="rocket_launch" size="55px" />
        </div>
        <div class="text-h6 text-bold">Multiple DEs</div>

        <p>
          XeroLinux Comes in 2 editions, "Main (KDE) Edition" and "XFCE
          edition".
        </p>
      </div>

      <div class="column feature">
        <div class="flex flex-center">
          <q-icon color="info" name="school" size="55px" />
        </div>
        <div class="text-h6 text-bold">Made for everyone</div>

        <p>
          If performance is more important to you, and you want to try out
          XeroLinux; check out the XFCE edition
        </p>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.feature {
  width: 400px;
  text-align: center;
}
</style>
