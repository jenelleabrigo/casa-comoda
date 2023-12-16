<template lang="">
  <header class="l-header">
    <div class="l-header__logo">
      <img src="~/assets/images/icons/img-logo.svg" alt="Casa Comoda Logo" class="l-header__logo__img" />
    </div>
    <nav class="l-nav">
      <nuxt-link to="#about" class="l-nav__link">About</nuxt-link>
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
<script>
export default {};
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

  &__socials {
    &__link {
      display: inline-flex;
      transition: 0.3s;

      &:not(:last-child) {
        margin-right: 1rem;
      }

      &:hover {
        scale: 1.1;
      }
    }
  }
}

.l-nav {
  &__link {
    position: relative;
    color: inherit;
    text-decoration: none;
    font-size: 1.6rem;
    font-weight: 500;

    &:not(:last-child) {
      margin-right: 4rem;
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
