<template>
  <div>
    <div class="selected-work wrapper">
      <div class="container">
        <h2 class="syne">Selected Work 🙌</h2>
      </div>
      <div class="work"></div>
      <swiper
        :slidesPerView="2.5"
        :spaceBetween="20"
        :pagination="{
          clickable: true,
        }"
        :modules="modules"
        class="mySwiper"
      >
        <swiper-slide>
          <NuxtLink to="/projects/halto"
            ><img src="/thumbnails/halto.png" alt="" /></NuxtLink></swiper-slide
        ><swiper-slide>
          <NuxtLink to="/projects/newgo"
            ><img src="/thumbnails/newgo.png" alt="" /></NuxtLink></swiper-slide
        ><swiper-slide>
          <NuxtLink to="/projects/doritos"><img src="/thumbnails/doritos.png" alt="" /></NuxtLink
        ></swiper-slide>
      </swiper>
      <div class="btn-container wrapper">
        <div class="container">
          <NuxtLink to="/projects" class="btn">All projects</NuxtLink>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/css";

import "swiper/css/pagination";

// import required modules
import { Pagination } from "swiper";

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [Pagination],
    };
  },
};
</script>

<style lang="scss">
.selected-work {
  overflow: hidden;
  flex-direction: column;
  align-items: center;
  padding-top: 100px;
  .container {
    h2 {
      font-size: 3.125rem;
      color: var(--blue);
    }
  }
  .work {
    margin-top: 30px;
    display: flex;
    gap: 20px;
    width: 100%;
    overflow-y: scroll;
    // overflow: visible;
    img {
      width: 630px;
    }
  }
  .btn-container {
    margin-top: 20px;
    padding-bottom: 20px;
    .container {
      display: flex;
      justify-content: flex-end;
    }
  }
}

.swiper {
  width: 100%;
  margin-left: 3%;
  padding-right: 5%;
  .swiper-slide {
    width: 630px;
    img {
      width: 100%;
      height: auto;
    }
  }
}

.swiper-pagination {
  display: none;
}
</style>
