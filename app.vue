<template lang="">
  <div>
    <Header />

    <div class="l-content">
      <Hero />
      <AboutUs />
      <Amenities />
      <AzureUrbanResort />
      <TheUnit />
    </div>

    <footer class="l-footer">©casacomoda2023</footer>
  </div>
</template>
<script setup>
import { register } from "swiper/element/bundle";
register();
const appConfig = useAppConfig();
</script>
<style lang="scss">
.l-content {
  // margin-top: 8rem;
}

.l-footer {
  font-size: 1.6rem;
  color: #fff;
  background: $primary;
  padding: 1rem;
  text-align: center;
}

.swiper {
  overflow-x: hidden;
  overflow-x: clip;
  overflow-y: visible;
}

.swiper-button-prev,
.swiper-button-next {
  height: 3rem;
  width: 3rem;
  border: 1px solid $primary;
  border-radius: 100%;
  bottom: -8rem;
  top: auto;

  &::after {
    color: $primary;
    font-size: 1.5rem;
    font-weight: bold;
  }
}

.swiper-button-next {
  right: auto;
  left: 6rem;
}

.swiper-pagination {
  top: auto !important;
  bottom: -6.5rem;
  height: 0.2rem !important;
  width: calc(100% - 13rem) !important;
  left: auto !important;
  right: 0;

  .swiper-pagination-progressbar-fill {
    background: $primary;
  }
}
</style>
