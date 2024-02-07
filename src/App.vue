<script >
import AppMain from "./components/AppMain.vue"
import AppLogo from "./components/AppLogo.vue";
export default {
  name: "Pokedex",
  components: {
    AppMain,
    AppLogo
  }
}
</script>

<template>
  <AppLogo />

  <AppMain />
</template>

<style lang="scss">
@use "./assets/scss/style.scss"
</style>
