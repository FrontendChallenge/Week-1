<template>
  <div class="right-sidebar">
    
  </div><!-- /.right-sidebar -->
</template>

<script>
  export default {
    name: 'right-sidebar'
  }
</script>

<style lang="scss">
  .right-sidebar {
    bottom: 0;
    background-color: #fffbf5;
    right: 0;
    position: absolute;
    top: 0;
    transition: all .25s;
    width: 300px;

    @media (max-width: 1200px) {
      transform: translateX(100%);
    }
  }
</style>