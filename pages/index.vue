<template>
  <section class="container">
    <div>
      <TheHeader/>
    </div>
  </section>
</template>

<script>
import TheHeader from '~/components/TheHeader.vue'

export default {
  components: {
    TheHeader,
  }
}
</script>

<style>
.container {
  min-height: 100vh;
  /* background-image: url("~assets/images/gray-wall.jpg");
  background-size: cover;
  background-position: center center; */
}
</style>

