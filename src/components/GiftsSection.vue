<template>
  <section class="gifts">
    <div class="gifts__container">
      <div class="gifts__title">
        На каждый ремонт гарантировано подарок на ваш выбор :
      </div>
      <div class="gifts__buttons">
        <button ref="prev" class="gifts__back"></button>
        <button ref="next" class="gifts__next"></button>
      </div>
      <div class="gifts__swipper">
        <Swiper
          :navigation="{
            prevEl: prev,
            nextEl: next,
          }"
          :pagination="{ clickable: true, el: '.gifts__pagination' }"
          :slides-per-view="4"
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
              slidesPerView: 4,
            },
            1240: {
              slidesPerView: 4,
            },
            1650: {
              slidesPerView: 4,
            },
          }"
        >
          <swiper-slide>
            <div class="gifts__card">
              <img src="@/assets/img/gifts/case.png" />
              <p>Чехлы</p>
            </div>
          </swiper-slide>
          <swiper-slide
            ><div class="gifts__card">
              <img src="@/assets/img/gifts/glass.png" />
              <p>Защитные стёкла</p>
            </div></swiper-slide
          >

          <swiper-slide
            ><div class="gifts__card">
              <img src="@/assets/img/gifts/cabels.png" />
              <p>Кабели</p>
            </div></swiper-slide
          >
          <swiper-slide>
            <div class="gifts__card">
              <img src="@/assets/img/gifts/carholder.png" />
              <p>Car holder</p>
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="gifts__card">
              <img src="@/assets/img/gifts/charger.png" />
              <p>Зарядки</p>
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="gifts__card">
              <img src="@/assets/img/gifts/headphones.png" />
              <p>Наушники</p>
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="gifts__card">
              <img src="@/assets/img/gifts/memory.png" />
              <p>Другие ассексуары</p>
            </div>
          </swiper-slide>
        </Swiper>
        <div class="gifts__pagination"></div>
      </div>
    </div>
  </section>
</template>

<style lang="scss">
.gifts {
  margin-bottom: 16rem;
  &__title {
    @media (max-width: 48em) {
      font-size: 4rem;
    }
    font-family: "Bebas Neue", sans-serif;
    font-size: 5.6rem;
    color: #13171d;
    margin-bottom: 4rem;
    max-width: 96rem;
  }
  &__buttons {
    display: flex;
    gap: 1.6rem;
    justify-content: end;
  }
  &__next {
    height: 4.8rem;
    width: 4.8rem;
    background-image: url("../assets/img/icons/Arrow.svg");
    background-repeat: no-repeat;
    padding: 1rem 2rem;
    border-radius: 50%;
    border: none;
    background-color: white;
    background-position: center;
    background-size: 2.4rem 2.4rem;
    cursor: pointer;
  }
  &__pagination {
    margin-top: 4rem;
    text-align: center;
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
  &__card {
    position: relative;
    width: 30.2rem;
    height: 31rem;
    background-color: rgba(255, 255, 255, 0.514);
    border-radius: 3rem;
    margin-bottom: 2rem;
    margin-top: 2.5rem;
    box-shadow: 0px 50px 60px rgba(255, 107, 0, 0.08),
      0px 8px 10px rgba(255, 107, 0, 0.08);
    img {
      position: absolute;
      max-width: 30rem;
      z-index: 100;
      bottom: 7rem;
    }
    p {
      position: absolute;
      bottom: 2rem;
      left: 4rem;
      color: #13171d;
      font-size: 2.2rem;
      font-weight: 600;
    }
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
