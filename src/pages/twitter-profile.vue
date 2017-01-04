<template>
  <div class="twitter-profile">
    <div class="twitter-profile__wrapper">
      
      <profile-sidebar></profile-sidebar>

      <div class="twitter-profile__content">
        <content-navigation></content-navigation>

        <tweets></tweets>
      </div><!-- /.twitter-profile__content -->

      <right-sidebar></right-sidebar>

    </div><!-- /.twitter-profile__wrapper -->
  </div><!-- /.twitter-profile -->
</template>

<script>
  import ProfileSidebar from '../components/profile-sidebar.vue'
  import RightSidebar from '../components/right-sidebar.vue'
  import ContentNavigation from '../components/content-navigation.vue'
  import Tweets from '../components/tweets.vue'

  export default {
    name: 'twitter-profile',
    components: {
      ProfileSidebar, RightSidebar, ContentNavigation, Tweets
    }
  }
</script>

<style lang="scss">
  .twitter-profile {
    height: 1px;
    min-height: 100%;
    padding-top: 80px;

    @media (max-width: 768px) {
      padding-top: 60px;
    }

    &__wrapper {
      background-color: #f2eee8;
      min-height: 100%;
      padding-left: 300px;
      padding-right: 300px;
      position: relative;
      transition: all .25s;

      @media (max-width: 1200px) {
        overflow: hidden;
        padding-right: 0;
      }

      @media (max-width: 840px) {
        padding-left: 0px;
      }
    }

    &__content {
      padding: 40px;

      @media (max-width: 768px) {
        padding: 20px;
      }
    }
  }
</style>