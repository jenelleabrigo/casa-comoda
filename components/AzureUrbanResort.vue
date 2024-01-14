<template lang="">
  <div class="s-azure">
    <div class="u-layout">
      <div class="s-azure__inner">
        <h1 class="c-hdg01">The Azure Urban Resort</h1>
        <p class="s-azure__inner__txt">
          Located in Bicutan, Parañaque City, AZURE URBAN RESORT RESIDENCES brought the first ever large scale man-made beach concept to a residential development in the Philippines.
          <br />
          <br />
          A tropical-inspired residential community with the Paris Beach Club designed by international celebrity and icon Paris Hilton.
        </p>
        <div></div>
      </div>
    </div>
  </div>
</template>
<script setup></script>
<style lang="scss" scoped>
.s-azure {
  &__inner {
    padding: 8rem 0 16rem;

    @include mq_sp {
      padding: 8rem 0;
    }

    &__txt {
      margin: 4rem 0 8rem;
    }
  }
}
</style>
