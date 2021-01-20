<template>
  <div>
    <TheHeader @sidenavToggle="displaySidenav = !displaySidenav" />
    <TheSidenav :show="displaySidenav" @close="displaySidenav = false" />
    <Nuxt />
  </div>
</template>

<script>
import TheHeader from '../components/Navigation/TheHeader';
import TheSidenav from '../components/Navigation/TheSidenav';

export default {
  components: {
    TheHeader,
    TheSidenav
  },
  data() {
    return {
      displaySidenav: false
    }
  }
}

</script>

<style>
html, body {
  font-family: 'Open Sans', sans-serif;
  margin: 0;
  box-sizing: border-box;
  -webkit-font-smoothing: antialiased;
}
</style>
