<template>
  <div class="tweet">
    <div class="tweet__meta">
      <div class="tweet__date">1d</div><!-- /.tweet__date -->

      <div class="tweet__user tweet-user">
        <div class="tweet-user__avatar">
          <img src="https://pbs.twimg.com/profile_images/768529565966667776/WScYY_cq_400x400.jpg" alt="" />
        </div>
        <div class="tweet-user__name">jack</div>
        <div class="tweet-user__handle">@jack</div>
      </div><!-- /.tweet__user -->
    </div><!-- /.tweet__meta -->

    <div class="tweet__content">
      <div class="tweet__text">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud...</div><!-- /.tweet__text -->
    </div><!-- /.tweet__content -->

    <div class="tweet__toolbar">
      <div class="tweet__toolbar-left">
        <a href="#" class="tweet__action tweet__action--reply">
          <img src="/static/icons/reply.svg" alt="" />
        </a>

        <a href="#" class="tweet__action tweet__action--retweet">
          <img src="/static/icons/retweet.svg" alt="" />
          <span>20</span>
        </a>

        <a href="#" class="tweet__action tweet__action--like">
          <img src="/static/icons/like.svg" alt="" />
          <span>55</span>
        </a>

        <a href="#" class="tweet__action tweet__action--more-actions">
          <img src="/static/icons/more-actions.svg" alt="" />
        </a>
      </div><!-- /.tweet__toolbar-left -->

      <div class="tweet__toolbar__right">
        <a href="#" class="tweet__action tweet__action--details">
          <img src="/static/icons/tweet-details.svg" alt="" />
        </a>
      </div><!-- /.tweet__toolbar__right -->
    </div><!-- /.tweet__toolbar -->
  </div><!-- /.tweet -->
</template>

<script>
  import Tweet from './tweet.vue'

  export default {
    name: 'tweet',
    components: {
      Tweet
    }
  }
</script>

<style lang="scss">
  .tweet {
    border-bottom: 1px solid #f1ede6;
    color: #57575f;
    min-height: 100px;
    padding: 20px;
    padding-left: 80px;

    &:last-child {
      border-bottom: 1px solid transparent;
    }

    &__meta {
      position: relative;
      padding-right: 50px;
    }

    &__date {
      color: #c6c1b0;
      font-weight: 300;
      position: absolute;
      right: 0;
    }

    &__user {
      margin-bottom: 10px;
    }

    &-user {
      position: relative;

      &__avatar {
        left: -50px;
        position: absolute;

        img {
          border: 0;
          border-radius: 50%;
          height: 40px;
          width: 40px;
        }
      }

      &__name,
      &__handle {
        display: inline-block;
      }

      &__name {
        font-weight: 700;
      }

      &__handle {
        color: #c6c1b0;
        font-weight: 300;
      }
    }

    &__content {
      font-weight: 300;
    }

    &__toolbar {
      display: flex;
      flex: 0 0 100%;
      align-items: flex-start;
      justify-content: space-between;
      height: 20px;
      margin-top: 15px;
    }

    &__action {
      color: #c6c1b0;
      display: inline-block;
      float: left;
      font-size: 12px;
      font-weight: 300;
      line-height: 16px;
      margin-right: 20px;
      text-decoration: none;

      img {
        float: left;
        height: 16px;
        margin-right: 5px;
      }

      span {
        line-height: 16px;
      }

      &--reply {
        img {
          transform: rotateY(180deg);
        }
      }

      &--details {
        margin-right: 0;

        img {
          height: 20px;
        }
      }
    }
  }
</style>