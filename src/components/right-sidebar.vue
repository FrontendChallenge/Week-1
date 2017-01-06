<template>
  <div class="right-sidebar">
    <div class="trends">
      <div class="sidebar__heading">Philippines trends</div>
      <a href="#" class="trends__trend">#DONTSTOPLYRICVIDEO</a>
      <a href="#" class="trends__trend">#MLFTSltsComlicated</a>
      <a href="#" class="trends__trend">#TangaLangMoments</a>
      <a href="#" class="trends__trend">#a5WordsForYou</a>
      <a href="#" class="trends__trend">#5SOSDONTSTOPLYRICVIDEO</a>
      <a href="#" class="trends__trend">Happy Chicserific Day</a>
      <a href="#" class="trends__trend">Dr. Fluke</a>
      <a href="#" class="trends__trend">JaDine For TBYD The Movie</a>
      <a href="#" class="trends__trend">Galawang JaXel</a>
      <a href="#" class="trends__trend">JulQuen For OBTCHTheMovie</a>
    </div><!-- /.trends -->

    <div class="who-to-follow-container">
      <div class="sidebar__heading">Who to follow</div><!-- /.sidebar__heading -->

      <who-to-follow></who-to-follow>
    </div><!-- /.who-to-follow -->
  </div><!-- /.right-sidebar -->
</template>

<script>
  import WhoToFollow from './who-to-follow.vue'

  export default {
    name: 'right-sidebar',
    components: {
      WhoToFollow
    }
  }
</script>

<style lang="scss">
  .right-sidebar {
    bottom: 0;
    background-color: #fffbf5;
    right: 0;
    padding: 40px 30px;
    position: absolute;
    top: 0;
    transition: all .25s;
    width: 300px;

    @media (max-width: 1200px) {
      transform: translateX(100%);
    }

    .sidebar__heading {
      font-weight: 300;
      margin-bottom: 20px;
      text-transform: uppercase;
    }

    .trends {
      margin-bottom: 40px;

      &__trend {
        color: #80a8cc;
        font-weight: 300;
        text-decoration: none;
      }
    }
  }
</style>