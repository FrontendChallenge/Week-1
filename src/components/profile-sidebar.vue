<template>
  <div class="profile-sidebar">
    
  </div><!-- /.profile-sidebar -->
</template>

<script>
  export default {
    name: 'profile-sidebar'
  }
</script>

<style lang="scss">
  .profile-sidebar {
    bottom: 0;
    background-color: #80a8cc;
    left: 0;
    position: absolute;
    top: 0;
    transition: all .25s;
    width: 300px;

    @media (max-width: 840px) {
      transform: translateX(-300px);
      z-index: 8888;
    }
  }

  .show-profile-sidebar {
    .profile-sidebar {
      transform: translateX(0);
    }
  }
</style>