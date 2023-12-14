<script>
import { Navigation, Pagination, Scrollbar, A11y, Autoplay } from 'swiper/modules'
import { Swiper, SwiperSlide } from 'swiper/vue'

import 'swiper/css'
import 'swiper/css/navigation'
import 'swiper/css/pagination'
import 'swiper/css/scrollbar'

export default {
  components: {
    Swiper,
    SwiperSlide
  },
  setup() {
    return {
      slides: [
        { src: '/slide1.jpg', alt: 'Slide 1' },
        { src: '/slide2.jpg', alt: 'Slide 2' },
        { src: '/slide3.jpg', alt: 'Slide 3' },
        { src: '/slide4.jpg', alt: 'Slide 4' },
        { src: '/slide5.jpg', alt: 'Slide 5' }
      ],
      modules: [Navigation, Pagination, Scrollbar, A11y, Autoplay]
    }
  },
  methods: {
    onSwiper(swiper) {
      this.swiper = swiper
    }
  }
}
</script>

<template>
  <section class="slider">
    <h2 class="slider__title">Корпоративная жизнь</h2>
    <swiper
      :pagination="{ clickable: true }"
      :modules="modules"
      :slides-per-view="1"
      :space-between="100"
      :loop="true"
      :autoplay="{ delay: 3000 }"
      @swiper="onSwiper"
    >
      <swiper-slide v-for="(slide, index) in slides" :key="index">
        <img :src="slide.src" :alt="slide.alt" />
      </swiper-slide>
      <div class="swiper-pagination"></div>
    </swiper>

    <div @click="swiper.slideNext()" class="swiper-button-next"></div>
    <div @click="swiper.slidePrev()" class="swiper-button-prev"></div>
  </section>
</template>

<style lang="scss">
.slider {
  position: relative;
  padding-bottom: 74px;
  &__title {
    color: $black;
    font-size: 56px;
    font-style: normal;
    font-weight: 600;
    line-height: 100%;
    margin: 0 0 58px 70px;
  }
}
.swiper {
  width: 1110px;
  margin: auto;
  position: relative;
}

.swiper-button-next {
  position: absolute;
  top: 5px;
  right: 55px;
}

.swiper-button-prev {
  position: absolute;
  top: 5px;
  left: 1030px;
}

.swiper-button-next,
.swiper-button-prev {
  color: $burgundy;
  padding: 20px 30px;
  border-radius: 50%;
  background-color: #f0f0f0;
  transform: scale(0.6);
}

.swiper .swiper-pagination-bullet {
  height: 6px;
  border-radius: 0;
  flex-grow: 1;
  background: $black;
  opacity: 0, 1;
}
.swiper .swiper-pagination-bullet-active {
  background: $burgundy;
}

.swiper .swiper-pagination-horizontal {
  display: flex;
  justify-content: space-between;
}

.swiper {
  --add-bottom: 30px;
  padding-bottom: var(--add-bottom);
}
.swiper [class^='swiper-button-'] {
  top: calc(50% - var(--add-bottom) / 2);
}
</style>
