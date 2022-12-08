<template>
  <section class="completed-orders">
    <div class="completed-orders__container">
      <div class="completed-orders__up">
        <div class="completed-orders__title">Выполненные заказы</div>
        <div class="completed-orders__buttons">
          <button ref="prev" class="completed-orders__back"></button>
          <button ref="next" class="completed-orders__next"></button>
        </div>
      </div>
      <div class="completed-orders__swiper">
        <Swiper
          :navigation="{
            prevEl: prev,
            nextEl: next,
          }"
          :pagination="{ clickable: true, el: '.completed-orders__pagination' }"
          :slides-per-view="3"
          :space-between="30"
          :loop="true"
          :modules="modules"
        >
          <swiper-slide
            ><img src="@/assets/img/completed-orders/1.png" />
          </swiper-slide>
          <swiper-slide
            ><img src="@/assets/img/completed-orders/2.png"
          /></swiper-slide>

          <swiper-slide
            ><img src="@/assets/img/completed-orders/3.png"
          /></swiper-slide>
        </Swiper>
        <div class="completed-orders__pagination"></div>
      </div>
    </div>
  </section>
</template>

<style lang="scss">
.completed-orders {
  margin-bottom: 4rem;
  background: linear-gradient(180deg, #ebf3f8 0%, rgba(235, 243, 248, 0) 100%);
  padding: 8rem 0;
  &__title {
    @media (max-width: 48em) {
      font-size: 4rem;
    }
    font-family: "Bebas Neue", sans-serif;
    font-size: 5.6rem;
    color: #13171d;
    margin-bottom: 4rem;
  }
  &__pagination {
    margin-top: 4rem;
    text-align: center;
  }
  &__buttons {
    display: flex;
    gap: 1.6rem;
  }
  &__up {
    display: flex;
    justify-content: space-between;
  }
  &__next {
    height: 4.8rem;
    width: 4.8rem;
    background-image: url("../assets/img/icons/Arrow.svg");
    background-repeat: no-repeat;
    padding: 1rem 2rem;
    background-size: 2.4rem 2.4rem;
    border-radius: 50%;
    border: none;
    background-color: white;
    background-position: center;
    cursor: pointer;
  }
  &__back {
    height: 4.8rem;
    width: 4.8rem;
    background-image: url("../assets/img/icons/Arrow.svg");
    background-repeat: no-repeat;
    background-size: 2.4rem 2.4rem;
    padding: 1rem 2rem;
    border-radius: 50%;
    border: none;
    background-color: white;
    background-position: center;
    transform: rotate(180deg);
    cursor: pointer;
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
