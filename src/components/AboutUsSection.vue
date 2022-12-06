<template>
  <section class="about-us">
    <div class="about-us__container">
      <div class="about-us__title">
        В нашей компании работают лучшие специалисты, которые прекрасно
        разбираются в современных технологиях и имеют более 3-х лет опыта
        работы.
      </div>
      <div class="about-us__main">
        <div class="about-us__text">
          <p>
            За счет этого мы гарантируем устранение любых неполадок и
            предоставляем гарантию на все выполненные работы.
          </p>
          <p>
            Мы поможем не только восстановить работоспособность техники, но и
            подскажем, как избежать возникновения подобных поломок в будущем.
          </p>
          <p>
            Квалифицированная консультация специалиста поможет безопасно
            пользоваться компьютером. В нашем штате работают опытные
            специалисты.
          </p>
        </div>
        <div class="about-us__swiper">
          <button ref="prev" class="about-us__prev"></button>
          <Swiper
            :navigation="{
              prevEl: prev,
              nextEl: next,
            }"
            :pagination="{ clickable: true, el: '.about-us__pagination' }"
            :slides-per-view="1"
            :loop="true"
            :modules="modules"
          >
            <swiper-slide
              ><img src="@/assets/img/about-us/1.png" />
            </swiper-slide>
            <swiper-slide
              ><img src="@/assets/img/about-us/1.png"
            /></swiper-slide>

            <swiper-slide
              ><img src="@/assets/img/about-us/1.png"
            /></swiper-slide>
          </Swiper>
          <button ref="next" class="about-us__next"></button>
          <div class="about-us__pagination"></div>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss">
.about-us {
  margin-bottom: 4.5rem;
  &__prev {
    position: absolute;
    top: 25rem;
    z-index: 10;
    left: -3rem;
    height: 4.8rem;
    width: 4.8rem;
    background-image: url("../assets/img/icons/Arrow.svg");
    background-repeat: no-repeat;
    padding: 1rem 2rem;
    border-radius: 50%;
    border: none;
    background-color: white;
    background-position: center;
    transform: rotate(180deg);
    cursor: pointer;
  }
  &__next {
    position: absolute;
    top: 25rem;
    z-index: 10;
    right: -3rem;
    height: 4.8rem;
    width: 4.8rem;
    background-image: url("../assets/img/icons/Arrow.svg");
    background-repeat: no-repeat;
    padding: 1rem 2rem;
    border-radius: 50%;
    border: none;
    background-color: white;
    background-position: center;
    cursor: pointer;
  }
  &__pagination {
    margin-top: 2rem;
    text-align: center;
  }
  &__main {
    display: flex;
    justify-content: space-between;
  }
  &__text {
    display: flex;
    flex-direction: column;
    gap: 2.4rem;
    max-width: 47rem;
    color: #646464;
    font-size: 1.8rem;
  }
  &__title {
    position: relative;
    margin: 0 auto;
    color: #13171d;
    font-size: 2.4rem;
    max-width: 70rem;
    font-weight: 500;
    text-align: center;
    margin-bottom: 15rem;
    &::before {
      content: "";
      position: absolute;
      background-image: url("../assets/img/icons/quotes.svg");
      background-position: center;
      top: -2rem;
      left: -4rem;
      width: 2.9rem;
      height: 2rem;
    }
    &::after {
      content: "";
      position: absolute;
      background-image: url("../assets/img/icons/quotes.svg");
      background-position: center;
      bottom: -2rem;
      right: -4rem;
      width: 2.9rem;
      height: 2rem;
      transform: rotate(180deg);
    }
  }
  &__swiper {
    max-width: 63.5rem;
    position: relative;
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
