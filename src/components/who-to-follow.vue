<template>
  <div class="who-to-follow">
    <div class="follow-user">
      <div class="follow-user__meta">
        <div class="follow-user__avatar">
          <img src="https://pbs.twimg.com/profile_images/768529565966667776/WScYY_cq_400x400.jpg" alt="" />
        </div>
        <div class="follow-user__name">jack</div>
        <button class="follow-user__button">+</button>
      </div><!-- /.follow-user__meta -->

      <div class="follow-user__description">CEO @ Twitter</div>
    </div><!-- /.follow-user -->

    <div class="follow-user">
      <div class="follow-user__meta">
        <div class="follow-user__avatar">
          <img src="https://pbs.twimg.com/profile_images/745553396015505408/E7b52fGn_bigger.jpg" alt="" />
        </div>
        <a class="follow-user__name" href="http://twitter.com/dgrubelic">Davor Grubelić</a>
        <button class="follow-user__button">+</button>
      </div><!-- /.follow-user__meta -->

      <div class="follow-user__description">Frontend developer</div>
    </div><!-- /.follow-user -->
  </div><!-- /.who-to-follow -->
</template>



<script>
  export default {
    name: 'who-to-follow'
  }
</script>

<style lang="scss">
  .who-to-follow {
    font-weight: 300;
  }

  .follow-user {
    margin-bottom: 20px;
    padding-left: 60px;
    padding-right: 20px;
    position: relative;

    &:last-child {
      margin-bottom: 0;
    }

    &__avatar {
      border-radius: 50%;
      height: 48px;
      left: 0;
      overflow: hidden;
      position: absolute;
      width: 48px;

      img {
        height: inherit;
        width: inherit;
      }
    }

    &__name {
      color: inherit;
      text-decoration: none;
    }

    &__description {
      color: #c6c1b0;
    }

    &__button {
      background-color: transparent;
      border: 1px solid #c6c1b0;
      border-radius: 0;
      cursor: pointer;
      font-size: 12px;
      height: 20px;
      line-height: 16px;
      outline: none;
      position: absolute;
      right: 0;
      width: 20px;
      top: 2px;
    }
  }
</style>