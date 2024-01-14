<template lang="">
  <div class="s-unit">
    <div class="u-layout">
      <div class="s-unit__inner">
        <h1 class="c-hdg01">The Unit</h1>
        <p class="s-unit__inner__txt">
          Relax in our new, stylish 2-bedroom condo. Equipped with Fiber connection, Netflix and a kitchenette. Enjoy your morning coffee on the balcony overlooking the picturesque mountains of
          Baguio.
        </p>
        <div class="s-unit__inner__slider-container">
          <Swiper
            :slides-per-view="'auto'"
            :centered-slides="'true'"
            :loop="true"
            :spaceBetween="10"
            :navigation="true"
            :breakpoints="{
              750: {
                spaceBetween: 40,
              },
            }"
            :pagination="{
              type: 'progressbar',
            }"
            class="s-unit__inner__slider-container__slider"
          >
            <SwiperSlide class="s-unit__inner__slider-container__slider__item">
              <img src="~assets/images/unit/img-unit-1.png" alt="unit" class="s-unit__inner__slider-container__slider__item__img" loading="lazy" />
            </SwiperSlide>
            <SwiperSlide class="s-unit__inner__slider-container__slider__item">
              <img src="~assets/images/unit/img-unit-2.png" alt="unit" class="s-unit__inner__slider-container__slider__item__img" loading="lazy" />
            </SwiperSlide>
            <SwiperSlide class="s-unit__inner__slider-container__slider__item">
              <img src="~assets/images/unit/img-unit-3.png" alt="unit" class="s-unit__inner__slider-container__slider__item__img" loading="lazy" />
            </SwiperSlide>
            <SwiperSlide class="s-unit__inner__slider-container__slider__item">
              <img src="~assets/images/unit/img-unit-4.png" alt="unit" class="s-unit__inner__slider-container__slider__item__img" loading="lazy" />
            </SwiperSlide>
            <SwiperSlide class="s-unit__inner__slider-container__slider__item">
              <img src="~assets/images/unit/img-unit-5.png" alt="unit" class="s-unit__inner__slider-container__slider__item__img" loading="lazy" />
            </SwiperSlide>
            <SwiperSlide class="s-unit__inner__slider-container__slider__item">
              <img src="~assets/images/unit/img-unit-6.png" alt="unit" class="s-unit__inner__slider-container__slider__item__img" loading="lazy" />
            </SwiperSlide>
          </Swiper>
        </div>
      </div>
    </div>
  </div>
</template>
<script setup>
var imageCount = 20;
</script>
<style lang="scss" scoped>
.s-unit {
  overflow: hidden;

  &__inner {
    padding: 8rem 0 16rem;

    @include mq_sp {
      padding: 8rem 0;
    }

    &__txt {
      margin: 4rem 0 8rem;
    }

    &__slider-container {
      &__slider {
        overflow: visible;
        width: 80rem;
        margin: 0 auto;

        &__item {
          &__img {
            width: 100%;
            height: 54.3rem;
            object-fit: cover;
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
