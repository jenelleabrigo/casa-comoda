<template lang="">
  <div class="s-about">
    <div class="u-layout">
      <div class="s-about__inner">
        <h1 class="c-hdg01 is-white u-sp-only">About Us</h1>
        <div class="s-about__inner__img-container">
          <img src="~/assets/images/img-about.jpg" alt="about" class="s-about__inner__img-container__img" />
        </div>
        <div class="s-about__inner__txt-container">
          <h1 class="c-hdg01 is-white u-pc-only">About Us</h1>
          <p class="s-about__inner__txt-container__txt">
            Casa Cómoda is a staycation unit in Azure Urban Resort Residences located at Parañaque City which strives to provide a cozy and homey space to people who wish to experience the amenities
            of the Azure Urban. <br /><br />The name came from Spanish root words Casa which means “home” and Cómoda which means “comfortable” thus the goal comfortable home for guests.
          </p>
        </div>
      </div>
    </div>
  </div>
</template>
<script setup></script>
<style lang="scss" scoped>
.s-about {
  background: $primary;

  &__inner {
    display: flex;
    align-content: flex-start;
    justify-content: space-between;
    padding: 12.5rem 0;
    color: #fff;

    @include mq_sp {
      display: block;
      padding: 8rem 0;
    }

    .c-hdg01 {
      text-align: left;
    }

    &__img-container {
      margin-left: -8rem;
      border-top-right-radius: 3rem;
      border-bottom-right-radius: 3rem;
      overflow: hidden;

      @include mq_sp {
        margin-left: -2rem;
        margin-top: 4rem;
      }

      &__img {
        height: 100%;
        width: 100%;
        object-fit: cover;
      }
    }

    &__txt-container {
      flex-shrink: 0;
      max-width: 55rem;
      margin-left: 10rem;

      @include mq_sp {
        margin-left: 0;
        max-width: unset;
      }

      &__txt {
        margin-top: 4rem;
      }
    }
  }
}
</style>
