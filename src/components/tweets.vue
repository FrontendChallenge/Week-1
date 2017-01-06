<template>
  <div class="tweets">
    <tweet></tweet>
    <tweet></tweet>
    <tweet></tweet>
    <tweet></tweet>
    <tweet></tweet>
    <tweet></tweet>
  </div><!-- /.tweets -->
</template>

<script>
  import Tweet from './tweet.vue'

  export default {
    name: 'tweets',
    components: {
      Tweet
    }
  }
</script>

<style lang="scss">
  .tweets {
    background-color: #fffbf5;
    box-shadow: 0 1px 5px rgba(0,0,0,0.1);
  }
</style>