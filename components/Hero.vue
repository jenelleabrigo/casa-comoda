<template lang="">
  <div class="s-hero">
    <div class="u-layout">
      <div class="s-hero__inner">
        <div class="s-hero__inner__txt-container">
          <h1 class="s-hero__inner__txt-container__tagline">CREATING<br />MEMORIES<br />COMFORTABLY</h1>
          <p class="s-hero__inner__txt-container__desc">Experience the first large scale man-made beach and wave pool in the city of Parañaque while you stay at a cozy and comfortable space.</p>
          <nuxt-link to="https://airbnb.com/h/casa-comoda-condo-unit-rental-at-azure" target="_blank" class="s-hero__inner__txt-container__btn c-btn u-pc-only">BOOK NOW!</nuxt-link>
        </div>

        <div class="s-hero__inner__slider-container">
          <swiper-container
            :slidesPerView="3"
            :loop="true"
            :spaceBetween="10"
            :pagination="{
              type: 'progressbar',
            }"
            :autoplay="{
              delay: 2500,
            }"
            :modules="modules"
            :breakpoints="{
              750: {
                spaceBetween: 40,
              },
            }"
            class="s-hero__inner__slider-container__slider"
          >
            <swiper-slide class="s-hero__inner__slider-container__slider__item"
              ><img src="~assets/images/feature/img-feature-1.jpg" alt="feature" class="s-hero__inner__slider-container__slider__item__img" loading="lazy"
            /></swiper-slide>
            <swiper-slide class="s-hero__inner__slider-container__slider__item"
              ><img src="~assets/images/feature/img-feature-2.jpg" alt="feature" class="s-hero__inner__slider-container__slider__item__img" loading="lazy"
            /></swiper-slide>
            <swiper-slide class="s-hero__inner__slider-container__slider__item"
              ><img src="~assets/images/feature/img-feature-3.jpg" alt="feature" class="s-hero__inner__slider-container__slider__item__img" loading="lazy"
            /></swiper-slide>
            <swiper-slide class="s-hero__inner__slider-container__slider__item"
              ><img src="~assets/images/feature/img-feature-4.jpg" alt="feature" class="s-hero__inner__slider-container__slider__item__img" loading="lazy"
            /></swiper-slide>
            <swiper-slide class="s-hero__inner__slider-container__slider__item"
              ><img src="~assets/images/feature/img-feature-5.jpg" alt="feature" class="s-hero__inner__slider-container__slider__item__img" loading="lazy"
            /></swiper-slide>
            <swiper-slide class="s-hero__inner__slider-container__slider__item"
              ><img src="~assets/images/feature/img-feature-6.jpg" alt="feature" class="s-hero__inner__slider-container__slider__item__img" loading="lazy"
            /></swiper-slide>
          </swiper-container>
        </div>
      </div>
      <nuxt-link to="https://airbnb.com/h/casa-comoda-condo-unit-rental-at-azure" target="_blank" class="s-hero__inner__txt-container__btn c-btn u-sp-only">BOOK NOW!</nuxt-link>
    </div>
  </div>
</template>
<script setup></script>
<style lang="scss" scoped>
.s-hero {
  overflow: hidden;
  background: url("../assets/images/feature/img-bg.png") center center/cover;
  padding: 16rem 0;

  @include mq_sp {
    padding: 8rem 0;
  }

  &__inner {
    display: flex;

    @include mq_sp {
      display: block;
    }

    &__txt-container {
      padding-top: 6rem;
      margin-right: 3.7rem;

      @include mq_sp {
        margin-right: 0;
      }

      &__tagline {
        font-size: 5.5rem;
        font-weight: bold;
        margin-bottom: 3rem;

        @include mq_sp {
          font-size: 4rem;
        }
      }

      &__desc {
        max-width: 41.5rem;
        margin-bottom: 3rem;

        @include mq_sp {
          max-width: unset;
        }
      }

      &__btn {
        display: inline-block;

        @include mq_sp {
          margin-top: 6rem;
          position: relative;
          left: 50%;
          transform: translateX(-50%);
        }
      }
    }

    &__slider-container {
      width: 88.5rem;

      @include mq_sp {
        width: 45rem;
        margin-left: -6rem;
        margin-top: 4rem;
      }

      &__slider {
        &__item {
          &__img {
            height: 100%;
            width: 100%;
            object-fit: contain;
            border-radius: 3rem;
            box-shadow: 0.5rem 0.5rem 1rem rgba($color: #000000, $alpha: 0.5);

            @include mq_sp {
              border-radius: 1.5rem;
              box-shadow: 0.2rem 0.2rem 1rem rgba($color: #000000, $alpha: 0.5);
            }
          }
        }
      }
    }
  }
}
</style>
