<template lang="">
  <header class="l-header">
    <nuxt-link to="/" class="l-header__logo">
      <img src="~/assets/images/icons/img-logo.svg" alt="Casa Comoda Logo" class="l-header__logo__img" />
    </nuxt-link>
    <button type="button" @click="handleClick" class="l-header__hamburger u-sp-only">
      <span class="l-header__hamburger__line"></span>
      <span class="l-header__hamburger__line"></span>
      <span class="l-header__hamburger__line"></span>
    </button>
    <nav class="l-nav">
      <nuxt-link to="#about" class="l-nav__link">About Us</nuxt-link>
      <nuxt-link to="#amenities" class="l-nav__link">Amenities</nuxt-link>
      <nuxt-link to="#gallery" class="l-nav__link">Gallery</nuxt-link>
      <nuxt-link to="#testimonials" class="l-nav__link">Testimonials</nuxt-link>
      <nuxt-link to="#contactus" class="l-nav__link">Contact Us</nuxt-link>
    </nav>
    <div class="l-header__socials">
      <nuxt-link to="https://web.facebook.com/CasaComodaStaycation" target="_blank" class="l-header__socials__link"
        ><img src="~/assets/images/icons/icn-fb.svg" alt="facebook" class="l-header__socials__link__icn"
      /></nuxt-link>
      <nuxt-link to="https://www.instagram.com/2023casacomoda/" target="_blank" class="l-header__socials__link"
        ><img src="~/assets/images/icons/icn-ig.svg" alt="instagram" class="l-header__socials__link__icn"
      /></nuxt-link>
      <nuxt-link to="https://www.tiktok.com/@casa.comoda.stayc" target="_blank" class="l-header__socials__link"
        ><img src="~/assets/images/icons/icn-tiktok.svg" alt="tiktok" class="l-header__socials__link__icn"
      /></nuxt-link>
      <nuxt-link to="https://airbnb.com/h/casa-comoda-condo-unit-rental-at-azure" target="_blank" class="l-header__socials__link"
        ><img src="~/assets/images/icons/icn-airbnb.svg" alt="airbnb" class="l-header__socials__link__icn"
      /></nuxt-link>
    </div>
  </header>
</template>
<script setup>
const count = ref(false);
const handleClick = () => {
  alert("click!");
};
</script>
<style lang="scss" scoped>
.l-header {
  padding: 1rem 8rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
  position: fixed;
  width: 100%;
  height: 8rem;
  top: 0;
  left: 0;
  z-index: 10;
  // background: #fff;

  @include mq_sp {
    padding: 1rem;
    height: 6rem;
    background: #fff;
  }

  &__logo {
    display: flex;
    align-content: center;
    justify-content: center;

    &__img {
      @include mq_sp {
        width: 9rem;
      }
    }
  }

  &__socials {
    @include mq_sp {
      position: fixed;
      bottom: 1rem;
      right: 1rem;
      display: flex;
      flex-direction: column;
    }

    &__link {
      display: inline-flex;
      transition: 0.3s;

      &:not(:last-child) {
        margin-right: 1rem;

        @include mq_sp {
          margin-right: 0;
          margin-bottom: 1rem;
        }
      }

      &:hover {
        scale: 1.1;
      }
    }
  }

  &__hamburger {
    @include mq_sp {
      background: none;
      border: 0;
      height: 2rem;
      width: 3rem;
      display: flex;
      justify-content: space-between;
      flex-direction: column;
      position: relative;
      z-index: 1;

      &__line {
        display: block;
        height: 0.2rem;
        width: 100%;
        background: $primary;
      }
    }
  }
}

.l-nav {
  @include mq_sp {
    display: none;
    position: fixed;
    top: 0;
    bottom: 0;
    left: 0;
    background: $primary;
    color: #fff;
    width: 100%;
    text-align: center;
  }

  &__link {
    position: relative;
    color: inherit;
    text-decoration: none;
    font-size: 1.6rem;
    font-weight: 500;

    @include mq_sp {
      display: block;
      padding: 2rem 0;
    }

    &:not(:last-child) {
      margin-right: 4rem;

      @include mq_sp {
        margin-right: 0;
        margin-bottom: 0;
      }
    }

    &::after {
      position: absolute;
      content: "";
      width: 0;
      height: 0.1rem;
      background: $primary;
      bottom: -0.2rem;
      left: 0;
      right: 0;
      margin: auto;
      transition: 0.3s;
    }

    &:hover {
      &::after {
        width: 100%;
      }
    }
  }
}
</style>
