<template lang="">
  <div>
    <Header />

    <div class="l-content">
      <Hero />
      <AboutUs />
      <Amenities />
      <AzureUrbanResort />
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
</style>
