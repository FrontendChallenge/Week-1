<template>
  <div id="app" class="app" v-bind:class="{'show-profile-sidebar': showProfileSidebar}">
    <app-header v-on:toggle-profile-sidebar="toggleProfileSidebar()"></app-header>

    <div class="app__wrapper">
      <twitter-profile></twitter-profile>
    </div><!-- /.app__wrapper -->
  </div>
</template>

<script>
import enquire from 'enquire.js'
import AppHeader from './components/app-header.vue'
import TwitterProfile from './pages/twitter-profile.vue'

export default {
  name: 'app',
  components: {
    AppHeader, TwitterProfile
  },

  created () {
    let that = this

    this.profileSidebarToggleMediaQuery = {
      match () {
        that.showProfileSidebar = false
      },

      unmatch () {
        that.showProfileSidebar = true
      }
    }

    if (window.outerWidth <= 840) {
      this.showProfileSidebar = false
    }

    enquire.register('screen and (max-width: 840px)', this.profileSidebarToggleMediaQuery)
  },

  destroyed () {
    enquire.unregister('screen and (max-width: 840px)', this.profileSidebarToggleMediaQuery)
  },

  data () {
    return {
      showProfileSidebar: true
    }
  },

  methods: {
    toggleProfileSidebar () {
      this.showProfileSidebar = !this.showProfileSidebar
    }
  }
}
</script>

<style lang="scss">
  $fa-font-path: "../node_modules/font-awesome/fonts";
  @import "../node_modules/font-awesome/scss/font-awesome.scss";
  
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
</style>