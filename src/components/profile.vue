<template>
  <div class="profile">
    <div class="profile__avatar">
      <img src="https://pbs.twimg.com/profile_images/768529565966667776/WScYY_cq_400x400.jpg" alt="" />
    </div><!-- /.profile__avatar -->

    <div class="profile__name">jack</div><!-- /.profile__name -->
    <div class="profile__description">@jack has no description so his profile is pretty boring. I had to come up with my own...</div><!-- /.profile__description -->

    <div class="profile__link"><i class="fa fa-link"></i> twitter.com</div><!-- /.profile__link -->

    <div class="profile__controls">
      <button class="button profile__follow">Follow</button>
    </div><!-- /.profile__controls -->

    <div class="profile__gallery">
      <div class="profile__gallery-media">
        <div class="profile__media">
          <img src="https://pbs.twimg.com/media/C1C97tgVIAAbv4y.jpg:thumb" alt="" />
        </div>
        <div class="profile__media">
          <img src="https://pbs.twimg.com/media/C0u5EY4UAAAd7sZ.jpg:thumb" alt="" />
        </div>
        <div class="profile__media">
          <img src="https://pbs.twimg.com/media/CxA14j6VEAEB_qa.jpg:thumb" alt="" />
        </div>

        <div class="profile__media">
          <img src="https://pbs.twimg.com/media/CxA14j6VEAEB_qa.jpg:thumb" alt="" />
        </div>
        <div class="profile__media">
          <img src="https://pbs.twimg.com/media/C1C97tgVIAAbv4y.jpg:thumb" alt="" />
        </div>
        <div class="profile__media">
          <img src="https://pbs.twimg.com/media/C0u5EY4UAAAd7sZ.jpg:thumb" alt="" />
        </div>

        <div class="profile__media">
          <img src="https://pbs.twimg.com/media/C0u5EY4UAAAd7sZ.jpg:thumb" alt="" />
        </div>
        <div class="profile__media">
          <img src="https://pbs.twimg.com/media/CxA14j6VEAEB_qa.jpg:thumb" alt="" />
        </div>
        <div class="profile__media">
          <img src="https://pbs.twimg.com/media/C1C97tgVIAAbv4y.jpg:thumb" alt="" />
        </div>
      </div><!-- /.profile__gallery-container -->
    </div><!-- /.profile__gallery -->

    <div class="profile__activities profile-activities">
      <h3 class="profile__heading">Activities</h3>

      <ul class="profile-activities__list">
        <li class="profile_activities__activity profile-activity">
          <i class="profile-activity__icon fa fa-plus"></i>
          <span class="profile-activity__type">Followed</span>
          <a class="profile-activity__value" href="#">Eddie</a>
        </li>

        <li class="profile_activities__activity profile-activity">
          <i class="profile-activity__icon fa fa-reply"></i>
          <span class="profile-activity__type">Replied to</span>
          <a class="profile-activity__value" href="#">Alexander tweet</a>
        </li>

        <li class="profile_activities__activity profile-activity">
          <i class="profile-activity__icon fa fa-retweet"></i>
          <span class="profile-activity__type">Retweeted</span>
          <a class="profile-activity__value" href="#">Eric tweet</a>
        </li>

        <li class="profile_activities__activity profile-activity">
          <i class="profile-activity__icon fa fa-retweet"></i>
          <span class="profile-activity__type">Retweeted</span>
          <a class="profile-activity__value" href="#">Eric tweet</a>
        </li>

        <li class="profile_activities__activity profile-activity">
          <i class="profile-activity__icon fa fa-star"></i>
          <span class="profile-activity__type">Favorited</span>
          <a class="profile-activity__value" href="#">John tweet</a>
        </li>
      </ul>
    </div><!-- /.profile__activities -->
  </div><!-- /.profile -->
</template>

<script>
  export default {
    name: 'profile'
  }
</script>

<style lang="scss">
  .profile {
    color: #fff;
    font-weight: 300;
    padding: 0 25px;
    padding-top: 55px;
    text-align: center;

    &__avatar {
      border-radius: 50%;
      height: 100px;
      margin: 0 auto;
      margin-bottom: 20px;
      overflow: hidden;
      width: 100px;

      img {
        height: inherit;
        width: inherit;
      }
    }

    &__name {
      font-weight: 700;
      margin-bottom: 15px;
    }

    &__description {
      margin-bottom: 25px;
    }

    &__link {
      margin-bottom: 20px;
    }

    &__follow {
      background-color: #6c94b8;
      border: 0;
      border-radius: 32px;
      color: #fff;
      cursor: pointer;
      display: block;
      font-size: 14px;
      font-weight: 300;
      height: 40px;
      line-height: 40px;
      margin-bottom: 40px;
      outline: none;
      width: 100%;
    }

    &__gallery {
      margin: 0 -25px;
    }

    &__gallery-media {
      display: flex;
      flex: 0 0 300px;
      flex-direction: row;
      flex-wrap: wrap;
    }

    &__media {
      display: flex;
      flex: 0 0 100px;
      flex-direction: column;

      img {
        width: 100px;
      }
    }

    &__heading {
      font-size: 18px;
      font-weight: 300;
      margin-bottom: 20px;
      text-transform: uppercase;
    }

    &__activities {
      padding: 25px 0;
      text-align: left;
    }
  }

  .profile-activities {
    &__list {
      list-style-type: none;
    }
  }

  .profile-activity {
    margin-bottom: 10px;

    &__icon {
      color: #6c94b8;
      margin-right: 10px;
      width: 16px;
    }

    &__type {
      color: #6c94b8;
    }

    &__value {
      color: #fff;
    }
  }
</style>