<template>
  <swiper ref="mySwiper" :options="swiperOptions">
    <swiper-slide v-for="(item, index) in slides" :key="index">
      <img class="product-info-realted__img m-auto d-block" :src="item.url" />
    </swiper-slide>
  </swiper>
</template>

<script>
import { Swiper, SwiperSlide } from "vue-awesome-swiper";
import "swiper/css/swiper.css";

export default {
  name: "ProductInfoRelatedSlider",
  components: {
    Swiper,
    SwiperSlide,
  },
  data() {
    return {
      slides: [
        {
          url: "https://via.placeholder.com/200x400",
        },
        {
          url: "https://via.placeholder.com/200x400",
        },
        {
          url: "https://via.placeholder.com/200x400",
        },
        {
          url: "https://via.placeholder.com/200x400",
        },
        {
          url: "https://via.placeholder.com/200x400",
        },
        {
          url: "https://via.placeholder.com/200x400",
        },
        {
          url: "https://via.placeholder.com/200x400",
        },
        {
          url: "https://via.placeholder.com/200x400",
        },
        {
          url: "https://via.placeholder.com/200x400",
        },
      ],
      swiperOptions: {
        slidesPerView: 1,
        autoplay: true,
        breakpoints: {
          1400: {
            slidesPerView: 6,
          },
          1300: {
            slidesPerView: 5,
          },
          1100: {
            slidesPerView: 4,
          },
          900: {
            slidesPerView: 3,
          },
          550: {
            slidesPerView: 2,
          },
        },
      },
    };
  },
};
</script>
