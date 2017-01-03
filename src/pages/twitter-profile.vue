<template>
  <div class="twitter-profile">
    <app-header></app-header>

    <div class="twitter-profile__wrapper">
      
      <left-sidebar></left-sidebar>

      <div class="twitter-profile__content">
        <content-navigation></content-navigation>

        <tweets></tweets>
      </div><!-- /.twitter-profile__content -->

      <right-sidebar></right-sidebar>

    </div><!-- /.twitter-profile__wrapper -->
  </div><!-- /.twitter-profile -->
</template>

<script>
  import AppHeader from '../components/app-header.vue'
  import LeftSidebar from '../components/left-sidebar.vue'
  import RightSidebar from '../components/right-sidebar.vue'
  import ContentNavigation from '../components/content-navigation.vue'
  import Tweets from '../components/tweets.vue'

  export default {
    name: 'twitter-profile',
    components: {
      AppHeader, LeftSidebar, RightSidebar, ContentNavigation, Tweets
    }
  }
</script>

<style lang="scss">
  .twitter-profile {
    height: 1px;
    min-height: 100%;
    padding-top: 80px;

    &__wrapper {
      background-color: #f2eee8;
      min-height: 100%;
      padding-left: 300px;
      padding-right: 300px;
      position: relative;
    }

    &__content {
      padding: 40px;
    }
  }
</style>