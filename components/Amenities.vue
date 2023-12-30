<template lang="">
  <div class="s-amenities">
    <div class="u-layout">
      <div class="s-amenities__inner">
        <h1 class="c-hdg01">Amenities</h1>
        <div class="s-amenities__inner__lists">
          <div class="s-amenities__inner__lists__item">
            <div class="s-amenities__inner__lists__item__img-container">
              <img src="~/assets/images/amenities/img-roof-deck.png" alt="" />
            </div>
            <div class="s-amenities__inner__lists__item__txt-container">
              <h2 class="s-amenities__inner__lists__item__txt-container__ttl">The roof deck</h2>
              <p class="s-amenities__inner__lists__item__txt-container__desc">
                360 degrees view of Azure Urban Resort Residences environment. Sky, sunset, city, and amenities - these are the breathtaking views you can enjoy. <br /><br />Guests can access the area
                from 7 AM to 10 PM.
              </p>
            </div>
          </div>
          <div class="s-amenities__inner__lists__item">
            <div class="s-amenities__inner__lists__item__img-container">
              <img src="~/assets/images/amenities/img-roof-deck.png" alt="" />
            </div>
            <div class="s-amenities__inner__lists__item__txt-container">
              <h2 class="s-amenities__inner__lists__item__txt-container__ttl">The roof deck</h2>
              <p class="s-amenities__inner__lists__item__txt-container__desc">
                360 degrees view of Azure Urban Resort Residences environment. Sky, sunset, city, and amenities - these are the breathtaking views you can enjoy. <br /><br />Guests can access the area
                from 7 AM to 10 PM.
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script setup></script>
<style lang="scss">
.s-amenities {
  &__inner {
    padding: 16rem 0;

    &__lists {
      margin-top: 8rem;

      &__item {
        display: flex;
        align-content: flex-start;
        justify-content: space-between;

        @include mq_sp {
          display: block;
        }

        &:not(:last-child) {
          margin-bottom: 8rem;
        }

        &__txt-container {
          &__ttl {
            text-transform: capitalize;
            font-size: 3.2rem;
            font-weight: normal;
            margin-bottom: 2.4rem;
          }

          &__desc {
            //
          }
        }

        &__img-container {
          border-radius: 3rem;
          overflow: hidden;
          width: 50rem;
          flex-shrink: 0;
          margin-right: 8rem;

          @include mq_sp {
            margin-right: 0;
            width: 100%;
            height: 20rem;
            margin-bottom: 3rem;
          }

          &__img {
            @include mq_sp {
              height: 100%;
            }
          }
        }

        &:nth-child(even) & {
          &__img-container {
            order: 2;
            margin-right: 0;
            margin-left: 8rem;

            @include mq_sp {
              margin-left: 0;
            }
          }
        }
      }
    }
  }
}
</style>
