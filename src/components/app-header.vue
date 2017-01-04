<template>
  <div class="app-header">
    <div class="app-header__logo">
      <a href="#">
        <!-- <img src="/static/icons/twitter-logo--blue.svg" alt="" /> -->
        <i class="fa fa-twitter"></i>
      </a>
    </div><!-- /.app-header__logo -->

    <div class="app-header__left-navbar">
      <div class="app-header__profile-toggle">
        <button class="app-header__button" @click="toggleProfileSidebar()">
          <i class="fa fa-bars"></i>
        </button>
      </div><!-- /.app-header__profile-toggle -->

      <div class="app-header__compose">
        <button class="app-header__button">
          <img src="/static/icons/feather--white.svg" alt="" />
        </button>
      </div><!-- /.app-header__compose -->

      <div class="app-header__navigation">
        <button class="app-header__button">
          <img src="/static/icons/bell.svg" alt="" />
        </button>
        <button class="app-header__button">
          <img src="/static/icons/mail.svg" alt="" />
        </button>
        <button class="app-header__button">#</button>
      </div><!-- /.app-header__navigation -->
    </div><!-- /.app-header__left-navbar -->

    <div class="app-header__right-navbar">
      <div class="app-header__search">
        <input type="text" class="app-header__search-input" placeholder="Search" />
      </div><!-- /.app-header__search -->

      <div class="app-header__profile">
        <img src="/static/icons/blank-profile.png" alt="" />
      </div><!-- /.app-header__profile -->
    </div><!-- /.app-header__right-navbar -->
  </div><!-- /.app-header -->
</template>

<script>
  export default {
    name: 'app-header',

    methods: {
      toggleProfileSidebar () {
        this.$emit('toggle-profile-sidebar')
      }
    }
  }
</script>

<style lang="scss">
  .app-header {
    align-items: center;
    background-color: #fffbf5;
    box-shadow: 0 1px 5px rgba(0,0,0,0.1);
    display: flex;
    flex-direction: row;
    height: 80px;
    justify-content: space-between;
    left: 0;
    position: fixed;
    right: 0;
    top: 0;
    z-index: 9999;

    &__button {
      background-color: transparent;
      border: 1px solid #e3dfd8;
      border-radius: 50%;
      cursor: pointer;
      height: 40px;
      line-height: 40px;
      margin-top: 20px;
      outline: none;
      width: 40px;
    }

    &__profile-toggle {
      align-self: flex-start;
      border-right: 1px solid #f1ede6;
      display: none;
      height: 80px;
      text-align: center;
      width: 80px;

      .app-header__button {
        font-size: 14px;
        line-height: 32px;
      }

      @media (max-width: 840px) {
        display: block;
      }
    }

    &__left-navbar {
      align-self: flex-start;
      display: -moz-box;
      display: flex;
      flex: 1 0 auto;
    }

    &__compose {
      align-items: center;
      align-self: flex-start;
      border-right: 1px solid #f1ede6;
      height: 80px;
      text-align: center;
      width: 80px;

      .app-header__button {
        background-color: #80a8cc;
        border: 1px solid transparent;
        line-height: 40px;

        img {
          height: 20px;
          margin-top: 8px;
        }

        &:hover {
          background-color: #6c94b8;
        }
      }
    }

    &__navigation {
      align-self: flex-start;
      display: flex;
      flex: 1 0 auto;
      flex-direction: row;
      height: 80px;
      padding: 0 20px;

      .app-header__button {
        align-items: center;
        display: flex;
        font-size: 16px;
        font-weight: 700;
        flex-direction: column;
        line-height: 36px;
        margin-right: 20px;
        position: relative;
        text-align: center;

        &:hover {
          background-color: #e3dfd8;
        }

        img {
          height: 18px;
          left: 50%;
          margin-left: -9px;
          margin-top: -9px;
          position: absolute;
          top: 50%;
        }
      }
    }

    &__logo {
      color: #80a8cc;
      display: flex;
      left: 50%;
      height: 80px;
      margin-left: -20px;
      position: absolute;
      top: 0;

      a {
        color: #80a8cc;
        display: block;
        font-size: 40px;
        line-height: 40px;
        padding-top: 16px;
        height: 100%;
      }

      img {
        height: 40px;
      }
    }

    &__right-navbar {
      align-self: flex-end;
      display: flex;
    }

    &__search {
      align-self: flex-end;
      display: flex;
      height: 80px;
      flex-direction: column;
      justify-content: center;
      padding: 0 20px;
    }

    &__search-input {
      background: url(/static/icons/search.svg) 95% center no-repeat;
      background-size: 16px 16px;
      background-color: transparent;
      border: 1px solid #e3dfd8;
      border-radius: 20px;
      font-size: 14px;
      font-weight: 300;
      height: 40px;
      line-height: 40px;
      align-self: center;
      outline: none;
      padding: 0 14px;
      padding-right: 30px;

      &:focus {
        background-color: #fff;
      }

      &::placeholder {
        font-family: inherit;
        font-weight: 300;
      }
    }

    &__profile {
      align-self: flex-end;
      display: flex;
      height: 80px;
      flex-direction: column;
      justify-content: center;
      margin-right: 20px;

      img {
        border: 1px solid #e3dfd8;
        border-radius: 50%;
        height: 40px;
        width: 40px;
      }
    }
  }

  @media (max-width: 768px) {
    .app-header {
      height: 60px;

      &__profile-toggle,
      &__compose,
      &__logo,
      &__profile {
        height: 60px;
        padding: 0 14px;
        width: 60px;
      }

      &__button {
        height: 32px;
        line-height: 32px;
        margin-top: 14px;
        margin-right: 10px;
        width: 32px;
      }

      &__navigation {
        height: 60px;
        padding: 0 14px;

        .app-header__button {
          border-right: 0px;
          border-radius: 0;
          line-height: 32px;
          margin-right: 0;

          &:first-child {
            border-top-left-radius: 50%;
            border-bottom-left-radius: 50%;
          }

          &:last-child {
            border-right: 1px solid #e3dfd8;
            border-top-right-radius: 50%;
            border-bottom-right-radius: 50%;
          }
        }
      }

      &__logo {
        a {
          padding-top: 10px;
        }
      }

      &__search {
        height: 60px;
        padding: 0 14px;
        padding-right: 0;
      }

      &__search-input {
        height: 32px;
        width: 150px;
      }

      &__profile {
        margin-right: 0;
        padding: 0 14px;

        img {
          height: 32px;
          width: 32px;
        }
      }
    }
  }
</style>