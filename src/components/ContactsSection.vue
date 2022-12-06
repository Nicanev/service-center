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
          :modules="modules"
        >
          <swiper-slide><img src="@/assets/img/contact/1.png" /> </swiper-slide>
          <swiper-slide><img src="@/assets/img/contact/2.png" /></swiper-slide>

          <swiper-slide><img src="@/assets/img/contact/1.png" /></swiper-slide>
          <swiper-slide><img src="@/assets/img/contact/2.png" /></swiper-slide>
        </Swiper>
        <div class="contact__pagination"></div>
      </div>
    </div>
  </section>
</template>

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
