<template>
  <q-footer
    class="site-footer q-pa-sm background-positive text-center"
    color="negative"
  >
    <div :class="{ 'q-mb-sm': $q.screen.lt.md }">
      &copy; XeroLinux all rights reserved | Created by
      <a target="_blank" href="https://and249.netlify.app/"
        >Anindo Neel Dutta</a
      >
    </div>
  </q-footer>
</template>

<style lang="scss" scoped>
.site-footer {
  color: black;

  a {
    color: black;

    &:hover {
      text-decoration: none;
    }
  }
}
</style>
