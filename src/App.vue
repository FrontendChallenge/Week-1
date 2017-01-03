<template>
  <div id="app">
    <twitter-profile></twitter-profile>
  </div>
</template>

<script>
import TwitterProfile from './pages/twitter-profile.vue'

export default {
  name: 'app',
  components: {
    TwitterProfile
  }
}
</script>

<style lang="scss">
  *, html, body {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }

  html, body, #app {
    height: 1px;
    min-height: 100%;
  }

  body {
    font-family: Lato;
  }

  #app {
    min-width: 1366px;
  }
</style>