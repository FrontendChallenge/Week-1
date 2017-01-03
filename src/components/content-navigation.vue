<template>
  <div class="content-navigation">
    <ul class="content-navigation__list">
      <li class="content-navigation__item" v-bind:class="{'is-active': selectedItem === 'tweets'}">
        <a href="#" class="content-navigation__link" @click="selectItem('tweets')">
          <span class="content-navigation__title">Tweets</span>
          <span class="content-navigation__count">200</span>
        </a>
      </li><!-- /.content-navigation__item -->

      <li class="content-navigation__item" v-bind:class="{'is-active': selectedItem === 'media'}">
        <a href="#" class="content-navigation__link" @click="selectItem('media')">
          <span class="content-navigation__title">Photos/Videos</span>
          <span class="content-navigation__count">200</span>
        </a>
      </li><!-- /.content-navigation__item -->

      <li class="content-navigation__item" v-bind:class="{'is-active': selectedItem === 'following'}">
        <a href="#" class="content-navigation__link" @click="selectItem('following')">
          <span class="content-navigation__title">Following</span>
          <span class="content-navigation__count">200</span>
        </a>
      </li><!-- /.content-navigation__item -->

      <li class="content-navigation__item" v-bind:class="{'is-active': selectedItem === 'followers'}">
        <a href="#" class="content-navigation__link" @click="selectItem('followers')">
          <span class="content-navigation__title">Followers</span>
          <span class="content-navigation__count">1M</span>
        </a>
      </li><!-- /.content-navigation__item -->
    </ul><!-- /.content-navigation__list -->
  </div><!-- /.content-navigation -->
</template>

<script>
  export default {
    name: 'content-navigation',
    data () {
      return {
        selectedItem: 'tweets'
      }
    },

    methods: {
      selectItem (item) {
        this.selectedItem = item
      }
    }
  }
</script>

<style lang="scss">
  .content-navigation {
    background-color: #fffbf5;
    box-shadow: 0 1px 5px rgba(0,0,0,0.1);
    height: 80px;
    margin-bottom: 30px;

    &__list {
      display: flex;
      flex-direction: row;
      font-size: 14px;
      height: 100%;
      list-style-type: none;
      margin: 0;
      padding: 0;
    }

    &__item {
      height: 100%;
      text-align: center;
      width: 25%;

      &:after {
        background-color: #80a8cc;
        bottom: 0;
        content: '';
        display: block;
        height: 0px;
        left: 0;
        position: absolute;
        right: 0;
        transition: all .25s;
      }

      &.is-active {
        position: relative;

        &:after {
          height: 5px;
        }
      }
    }

    &__link {
      color: #605e58;
      display: block;
      height: 100%;
      outline: none;
      padding-top: 20px;
      text-decoration: none;
    }

    &__title {
      display: block;
      font-weight: 300;
      margin-bottom: 3px;
      text-transform: uppercase;
    }

    &__count {
      display: block;
      font-weight: 700;
    }
  }
</style>