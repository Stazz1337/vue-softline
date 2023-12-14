<script setup>
import Offices from './components/Offices.vue'
import Header from './components/Header.vue'
import Promo from './components/Promo.vue'
import About from './components/About.vue'
import Mission from './components/Mission.vue'
import Directions from './components/Directions.vue'
import Benefits from './components/Benefits.vue'
import Slider from './components/Slider.vue'


</script>

<template>
  <div class="wrapper">
    <Header />
    <Promo/>
    <About />
    <Offices/>
    <Mission/>
    <Directions />
    <Benefits/>
    <Slider/>
  </div>
</template>

<style scoped lang="scss">

.wrapper {
  width: 1250px;
  margin: auto;
}
</style>
