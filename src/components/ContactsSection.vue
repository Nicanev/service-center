<template>
  <section class="contact">
    <div class="contact__container">
      <div class="contact__title">Наши контакты</div>
      <div class="contact__swiper">
        <Swiper
          :navigation="{
            prevEl: prev,
            nextEl: next,
          }"
          :pagination="{ clickable: true, el: '.contact__pagination' }"
          :slides-per-view="4"
          :loop="true"
          :breakpoints="{
            310: {
              slidesPerView: 1,
            },
            640: {
              slidesPerView: 1,
            },
            768: {
              slidesPerView: 2,
            },
            1240: {
              slidesPerView: 3,
            },
            1650: {
              slidesPerView: 4,
            },
          }"
          :modules="modules"
        >
          <swiper-slide><img src="@/assets/img/contact/1.png" /> </swiper-slide>
          <swiper-slide
            ><img src="@/assets/img/contact/2.png" />
            <button></button>
          </swiper-slide>

          <swiper-slide><img src="@/assets/img/contact/1.png" /></swiper-slide>
          <swiper-slide
            ><img src="@/assets/img/contact/2.png" /><button></button
          ></swiper-slide>
        </Swiper>
        <div class="contact__pagination"></div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.swiper-slide {
  position: relative;
  img {
  }
  button {
    @media (max-width: 48em) {
      left: 25%;
    }
    height: 5.6rem;
    width: 5.6rem;
    border-radius: 50%;
    border: none;
    background-repeat: no-repeat;
    background-size: 1.8rem;
    position: absolute;
    background-color: white;
    background-image: url("../assets/img/icons/play.svg");
    background-position: center;
    top: 50%;
    left: 35%;
    transform: translate(-50%, -50%);
    outline: 0.8rem solid rgba(255, 255, 255, 0.486);
    cursor: pointer;
  }
}
</style>
<style lang="scss">
.contact {
  &__title {
    color: #13171d;
    font-size: 5.6rem;
    margin-bottom: 3rem;
  }
  &__pagination {
    margin-top: 4rem;
  }
}
</style>

<script>
import { ref } from "vue";
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/css";
import { Navigation, Pagination } from "swiper";
import "swiper/css/pagination";
export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    const prev = ref(null);
    const next = ref(null);
    return {
      modules: [Navigation, Pagination],
      prev,
      next,
    };
  },
};
</script>
