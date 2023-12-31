<template lang="">
  <div class="s-amenities">
    <div class="u-layout">
      <div class="s-amenities__inner">
        <h1 class="c-hdg01">Amenities</h1>
        <div class="s-amenities__inner__lists" :class="{ showAll: isOpen }">
          <div class="s-amenities__inner__lists__item" v-for="item in amenities">
            <div class="s-amenities__inner__lists__item__img-container">
              <img src="~/assets/images/amenities/img-beach-club.png" alt="" class="s-amenities__inner__lists__item__img-container__img" />
            </div>
            <div class="s-amenities__inner__lists__item__txt-container">
              <h2 class="s-amenities__inner__lists__item__txt-container__ttl">{{ item.title }}</h2>
              <p class="s-amenities__inner__lists__item__txt-container__desc">{{ item.description }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="s-amenities__more" :class="{ up: isOpen }">
      <p @click="isOpen = !isOpen" class="c-caret">{{ isOpen ? "SEE LESS" : "SEE MORE" }}</p>
    </div>
  </div>
</template>
<script setup>
const isOpen = ref(false);

const amenities = ref([
  {
    id: 1,
    title: "The roof deck",
    description:
      "360 degrees view of Azure Urban Resort Residences environment. Sky, sunset, city, and amenities - these are the breathtaking views you can enjoy.\n\nGuests can access the area from 7 AM to 10 PM.",
    image: "img-roof-deck.png",
  },
  {
    id: 2,
    title: "Paris Beach Club",
    description:
      "Paris Beach Club is at the center of Azure Urban Resort Residences where many amenities are located. Concierge, lounge, candy bar, children’s playroom, and locker rooms are located at its ground floor. Spa, gym and studio, game room, and movie room are located at the second floor which are exclusive for owners and residents only. Al Fresco dining and function hall are located at the third floor.",
    image: "img-beach-club.png",
  },
  {
    id: 3,
    title: "Wave Pool",
    description:
      "Experience the waves at 8:30AM, 9:30AM, 10:30AM, and 11:30AM for morning shift and 2:30PM, 3:30PM, 4:30PM, and 5:30PM for afternoon shift. \n\nOpen from 7AM-12PM and 2PM-7PM for P250/head per shift. Kids below 3ft are free of charge.",
    image: "img-wave-pool.png",
  },
  {
    id: 4,
    title: "Kiddie Beach",
    description: "Kids can enjoy the sand and beach with slide.  Beach is open from 7AM-12PM and 2PM-7PM.",
    image: "img-kiddie-beach.png",
  },
  {
    id: 5,
    title: "Lap Pool",
    description:
      "Lap pool has 5 swimmers lane and an overlooking view of the wave pool. It is exclusive for unit owners, residents, and long term guests registered as residents.\n\nIt is open daily from 7AM to 9PM.",
    image: "img-lap-pool.png",
  },
  {
    id: 6,
    title: "Lagoon 1",
    description:
      "Located between towers A and B. Lagoon pools are exclusive for unit owners, residents, and long term guests registered as residents.\n\nLagoon 1 is open daily from 7AM to 7PM except on Tuesdays for its weekly cleaning and maintenance.",
    image: "img-lagoon-1.png",
  },
  {
    id: 7,
    title: "Lagoon 2",
    description:
      "Located between towers A and B. Lagoon pools are exclusive for unit owners, residents, and long term guests registered as residents.\n\nLagoon 2 is open daily from 7AM to 9PM except on Wednesdays for its weekly cleaning and maintenance.",
    image: "img-lagoon-2.png",
  },
  {
    id: 8,
    title: "Basketball Court",
    description: "Located just beside the Paris beach Club with prior approval of use is required. The court is open for reservation from 7AM to & 7PM.",
    image: "img-basketball.png",
  },
  {
    id: 9,
    title: "Volleyball Court",
    description: "Bring you ball and play volleyball on sand. Located just beside the lap pool with prior approval of use is required. The court is open for reservation from 7AM to & 5PM.",
    image: "img-volleyball.png",
  },
  {
    id: 10,
    title: "Gym & Studio",
    description:
      "Stay healthy and fit! The gym is exclusive for unit owners, residents, and long term guests registered as residents. Located at the second floor of Paris Beach Club.\n\nIt is open daily from 6AM to 9PM.",
    image: "img-gym.png",
  },
  {
    id: 11,
    title: "Movie Room",
    description:
      "Experience theater-feels when watching movie at Azure Urban. The movie room is exclusive for unit owners, residents, and long term guests registered as residents.\n\nThere are three screening schedule available per day - 9AM to 12PM, 1PM to 4PM, and 6PM to 9PM. Located at the second floor of Paris Beach Club.\n\nIt is open daily from 9AM to 9PM.",
    image: "img-movie-room.png",
  },
  {
    id: 12,
    title: "Game Room",
    description:
      "Game room has PS4, PS5, and air hockey to choose from. It is exclusive for unit owners, residents, and long term guests registered as residents. Located at the second floor of Paris Beach Club.\n\nTIt is open daily from 9AM to 9PM.",
    image: "img-game-room.png",
  },
  {
    id: 13,
    title: "Playroom",
    description: "Located at the ground floor of Paris Beach Club open from 9AM to 7PM exclusive for owners and residents’ children below 12 feet.",
    image: "img-playroom.png",
  },
  {
    id: 14,
    title: "Locker Room",
    description:
      "Male and female locker rooms are located at the ground floor of Paris Beach Club. It is furnished with restrooms, shower rooms, and cabinets.\n\nGuests can access the area from 7AM to 9PM.",
    image: "img-locker.png",
  },
]);
</script>
<style lang="scss">
.s-amenities {
  position: relative;

  &__inner {
    padding: 16rem 0 8rem;

    @include mq_sp {
      padding: 8rem 0;
    }

    &__lists {
      margin-top: 8rem;
      height: 150rem;
      overflow: hidden;

      &.showAll {
        height: auto;
      }

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
            white-space: pre-wrap;
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
            border-radius: 3rem;
            height: 100%;
            width: 100%;
            object-fit: cover;
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

  &__more {
    position: absolute;
    height: 45rem;
    background: linear-gradient(transparent, rgba(255, 255, 255, 0.8), #fff);
    width: 100%;
    bottom: 0;
    transition: 0.3s;

    .c-caret {
      cursor: pointer;
    }

    &.up {
      height: 0;
    }

    &.up .c-caret {
      &::after {
        transform: rotate(-135deg);
        left: 2rem;
      }
    }
  }
}
</style>
