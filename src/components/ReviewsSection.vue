<template>
  <section class="reviews">
    <div class="reviews__container">
      <div class="reviews__up">
        <div class="reviews__title">Отзывы счастливых клиентов</div>
        <div class="reviews__buttons">
          <button ref="prev" class="reviews__back"></button>
          <button ref="next" class="reviews__next"></button>
        </div>
      </div>
      <div class="reviews__swiper">
        <Swiper
          :navigation="{
            prevEl: prev,
            nextEl: next,
          }"
          :pagination="{ clickable: true, el: '.reviews__pagination' }"
          :slides-per-view="3"
          :loop="true"
          :modules="modules"
          :breakpoints="{
            310: {
              slidesPerView: 1,
            },
            640: {
              slidesPerView: 1,
            },
            768: {
              slidesPerView: 3,
            },
            1240: {
              slidesPerView: 3,
            },
            1650: {
              slidesPerView: 4,
            },
          }"
        >
          <swiper-slide
            ><img src="@/assets/img/about/review1.png" />
            <button></button>
          </swiper-slide>
          <swiper-slide
            ><img src="@/assets/img/about/review2.png" /><button></button
          ></swiper-slide>

          <swiper-slide
            ><img src="@/assets/img/about/review3.png" /><button></button
          ></swiper-slide>
        </Swiper>
        <div class="reviews__pagination"></div>
      </div>
    </div>
  </section>
</template>

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
<style lang="scss" scoped>
.swiper-slide {
  position: relative;
  img {
    width: 41.2rem;
    height: 40rem;
  }
  button {
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
    top: 40%;
    left: 16rem;

    outline: 0.8rem solid rgba(255, 255, 255, 0.486);
    cursor: pointer;
  }
}
</style>
<style lang="scss">
.reviews {
  margin-bottom: 4rem;
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

  &__up {
    display: flex;
    justify-content: space-between;
  }
  &__next {
    height: 4.8rem;
    width: 4.8rem;
    background-image: url("../assets/img/icons/Arrow.svg");
    background-size: 2.4rem 2.4rem;
    background-repeat: no-repeat;
    padding: 1rem 2rem;
    border-radius: 50%;
    border: none;
    background-color: white;
    background-position: center;
    cursor: pointer;
  }
  &__buttons {
    display: flex;
    gap: 1.6rem;
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
.swiper-pagination-bullet-active {
  background-color: white !important;
  border: 0.2rem solid #e2001a;
}
</style>
