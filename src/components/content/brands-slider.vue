<template>
  <section class="brands_slider_block">
    <div class="container">
      <div class="inner">
        <swiper
          :modules="[Autoplay, Navigation, Pagination]"
          :slides-per-view="3"
          :space-between="50"
          :autoplay="{ delay: 5000 }"
          :loop="true"
          :breakpoints="{
            320: { slidesPerView: 1, spaceBetween: 20 },
            768: { slidesPerView: 1, spaceBetween: 50 },
            900: { slidesPerView: 2, spaceBetween: 50 },
            1200: { slidesPerView: 3, spaceBetween: 50 },
          }"
          @swiper="onSwiper"
          @slideChange="onSlideChange"
        >
          <swiper-slide v-for="(image, index) in images" :key="index">
            <img :src="image" alt="Brand Logo" />
          </swiper-slide>
        </swiper>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'
import { Swiper, SwiperSlide } from 'swiper/vue'
import { Autoplay, Navigation, Pagination } from 'swiper/modules'
import 'swiper/css'

const images = ref([
  'images/brands/Clintons_logo.svg',
  'images/brands/EPM-Logo.svg',
  'images/brands/gaucho.svg',
  'images/brands/M-logo-small.png',
  'images/brands/MMS.webp',
  'images/brands/Shanly_Logo_June_2024.svg',
  'images/brands/TheBreatheCo_Logo_Green.svg',
  'images/brands/Tilia_Homes_Logo.svg',
  'images/brands/ups.svg',
  'images/brands/zestcode-logo_1.png',
])

const onSwiper = swiper => {
  console.log(swiper)
}
const onSlideChange = () => {
  console.log('slide change')
}
</script>

<script>
import { defineComponent } from 'vue'
import { Swiper, SwiperSlide } from 'swiper/vue'

export default defineComponent({
  components: {
    Swiper,
    SwiperSlide,
  },
})
</script>

<style lang="scss" scoped>
.brands_slider_block {
  padding: 50px 0px;
  .container {
    max-width: 1350px;
    margin: 0 auto;
    padding: 0px 25px;
    .inner {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 50px;
      background-color: #030f18;
      border-radius: 10px;
      overflow: hidden;
      .swiper {
        width: 100%;
        height: 100%;
        padding: 20px 0px;

        .swiper-slide {
          display: flex;
          justify-content: center;
          align-items: center;
          height: 90px;
          img {
            height: 100%;
            width: 100%;
            max-width: 200px;
            object-fit: contain;
          }
        }
      }
    }
  }
}
</style>
