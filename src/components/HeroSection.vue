<template>
  <section class="hero" id="hero">
    <div class="consult" v-if="isModalOpen">
      <div class="consult__cover" @click="isModalOpen = false"></div>
      <div class="consult__body">
        <div class="consult__title">
          Оставьте заявку на <span>бесплатную</span> консультацию
        </div>
        <form class="consult__form"></form>
      </div>
    </div>
    <div class="hero__container" :class="{ stealth: isModalOpen }">
      <div class="hero__main">
        <div class="hero__text">
          <div class="hero__title">
            Проблемы <br />
            с Вашим устройством?
            <img src="@/assets/img/hero/Arrow.svg" />
          </div>
          <div class="hero__subtitle">
            Решаем любые проблемы! <br />
            Большой склад и опытные мастера
          </div>
          <button class="hero__btn" @click="isModalOpen = true">
            Бесплатная консультация
          </button>
        </div>
        <div class="hero__img">
          <img src="@/assets/img/hero/Punktirline.svg" class="hero__line" />
          <img src="@/assets/img/hero/master2.png" class="hero__master" />
          <img src="@/assets/img/hero/gear.svg" class="hero__gear" />
          <img src="@/assets/img/hero/laptop.svg" class="hero__laptop" />
          <img src="@/assets/img/hero/monitor.svg" class="hero__monitor" />
          <img src="@/assets/img/hero/phone.svg" class="hero__phone" />
          <div class="hero__circle-big"></div>
          <img src="@/assets/img/hero/Wave.svg" class="hero__wave" />
          <div class="hero__stock stock">
            <div class="stock__body">
              <div class="stock__percent">50%</div>
              <div class="stock__title">
                скидка на ремонт телефонов, ноутбуков и планшетов до
                <span>-50%</span>
              </div>
              <div class="stock__end">
                <h1>Конец акции:</h1>
                <div class="stock__time">
                  <div class="stock__clock">
                    <span>2</span> <span>:</span> <span>18</span> <span>:</span>
                    <span>56</span>
                  </div>
                  <div class="stock__designations">
                    <span>DAYS</span> <span></span> <span>HOURS</span>
                    <span></span> <span>MINUTES</span>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="hero__advantages">
        <div class="hero__adv">
          <img src="@/assets/img/hero/adv1.svg" />
          <h1>Курьер по городу</h1>
        </div>
        <div class="hero__adv">
          <img src="@/assets/img/hero/adv2.svg" />
          <h1>Подменный телефон - Бесплатно</h1>
          <p>Телефон взамен Беслатно, пока ваш в ремонте</p>
        </div>
        <div class="hero__adv">
          <img src="@/assets/img/hero/adv3.svg" />
          <h1>Забота о вас</h1>
          <p>Незначительные поломки - делаем бесплатно.</p>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss">
.consult {
  position: fixed;
  z-index: 2;
  width: 100%;
  height: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  &__body {
    position: relative;
    z-index: 501;
    padding: 6rem 9rem;
    background-color: white;
    border-radius: 2rem;
  }
  &__cover {
    position: absolute;
    z-index: 500;
    height: 200vh;
    background: #13171d;
    opacity: 0.9;
    width: 100%;
  }
  &__title {
    font-family: "Bebas Neue", sans-serif;
    font-size: 3.2rem;
    text-align: center;
  }
}
.stock {
  @media (max-width: 48em) {
    display: none;
  }
  position: absolute;
  top: 20rem;
  right: 30rem;
  z-index: 10;
  &__clock {
    display: flex;
    gap: 0.7rem;
    span {
      color: #13171d;
      font-weight: 600;
      font-size: 3.2rem;
    }
  }
  &__designations {
    display: flex;
    gap: 0.7rem;
    span {
      font-size: 1.1rem;
      color: #13171d;
      opacity: 0.5;
      font-weight: 600;
    }
  }
  &__body {
    background-color: white;
    width: 26.4rem;
    height: 30.9rem;
    border-radius: 3rem;
    box-shadow: 0px 7.1rem 8rem rgba(255, 107, 0, 0.11),
      0px 2.14044rem 2.41177rem rgba(255, 107, 0, 0.0716748),
      0px 0.88903rem 1.00172rem rgba(255, 107, 0, 0.055),
      0px 0.321545rem 0.362304rem rgba(255, 107, 0, 0.0383252);
  }
  &__percent {
    color: #ff6b00;
    position: relative;
    bottom: 4rem;
    font-size: 11.3rem;
    font-family: "Bebas Neue", sans-serif;
    text-align: center;
    text-shadow: 0px 100px 80px rgba(255, 107, 0, 0.11),
      0px 46.233px 36.9864px rgba(255, 107, 0, 0.0815843),
      0px 26.4535px 21.1628px rgba(255, 107, 0, 0.0689459),
      0px 16.0571px 12.8457px rgba(255, 107, 0, 0.0593943),
      0px 9.67509px 7.74008px rgba(255, 107, 0, 0.0506057),
      0px 5.38772px 4.31018px rgba(255, 107, 0, 0.0410541),
      0px 2.31722px 1.85378px rgba(255, 107, 0, 0.0284157);
  }
  &__title {
    margin-top: -6rem;
    color: #13171d;
    font-size: 2rem;
    width: 21.3rem;
    margin-left: 3rem;
    span {
      font-weight: bold;
    }
  }
  &__end {
    margin-top: 2.2rem;
    margin-left: 3rem;
    padding-top: 2.2rem;
    width: 20.5rem;
    border-top: 0.1rem solid #e8e5e5;
    h1 {
      color: #13171d;
      font-weight: 600;
      font-size: 2rem;
      opacity: 0.5;
    }
  }
}
.hero {
  margin-bottom: 20rem;
  padding-top: 2.5rem;
  &__advantages {
    max-width: 130rem;
    display: flex;
    flex-wrap: wrap;
    position: relative;
    z-index: 10;
    justify-content: space-around;
  }
  &__adv {
    display: flex;
    flex-direction: column;
    gap: 1.8rem;
    img {
      width: 8rem;
      height: 8rem;
    }
    h1 {
      color: #13171d;
      font-size: 2rem;
      font-weight: 600;
    }
    p {
      font-size: 1.6rem;
      color: #444444;
      max-width: 34rem;
      line-height: 2.4rem;
    }
  }
  &__title {
    @media (max-width: 48em) {
      text-align: center;
      font-size: 7rem;
      margin-left: -5rem;
      width: 72rem;
    }
    font-family: "Bebas Neue", sans-serif;
    font-size: 11rem;
    color: --main-font-color;
    width: 73.1rem;
    line-height: 10rem;
    margin-left: 2.2rem;
    position: relative;
    img {
      position: absolute;
      top: 2.5rem;
      width: 8.8rem;
      right: 9rem;
    }
  }
  &__subtitle {
    margin-top: 2rem;
    color: #444444;
    font-size: 2.4rem;
    margin-left: 12.8rem;
    line-height: 3.4rem;
    margin-bottom: 4rem;
  }
  &__btn {
    color: white;
    background-color: #e2001a;
    border: none;
    border-radius: 1.5rem;
    padding: 1.8rem 3rem;
    font-size: 1.6rem;
    font-weight: 600;
    cursor: pointer;
    margin-left: 12.8rem;
  }
  &__text {
    position: relative;
    z-index: 10;
    margin-top: 29rem;
  }
  &__main {
    @media (max-width: 48em) {
      flex-direction: column-reverse;
    }
    display: flex;
  }
  &__container {
  }
  &__img {
    @media (max-width: 48em) {
      right: 0;
    }
    top: 7.5rem;
    position: relative;
    right: 12.5rem;
    max-height: 90rem;
  }
  &__wave {
    position: relative;
    bottom: 230rem;
    left: 85rem;
    width: 9.8rem;
    height: 6.2rem;
  }
  &__circle-big {
    position: relative;
    bottom: 150rem;
    right: 15rem;
    width: 105.6rem;
    height: 105.6rem;
    border-radius: 50%;
    background: conic-gradient(
      from 180deg at 50% 50%,
      #eef3f8 0deg,
      rgba(238, 243, 248, 0) 360deg
    );
    opacity: 0.6;
    z-index: 1;
  }
  &__monitor {
    position: relative;
    width: 5rem;
    height: 5rem;
    bottom: 77rem;
    z-index: 5;
    padding: 1.314rem;
    right: 10rem;
    background-color: white;
    border-radius: 50%;
    box-shadow: 0 2rem 4rem rgba(255, 107, 0, 0.13),
      0 1rem 1rem rgba(255, 107, 0, 0.05);
  }
  &__laptop {
    position: relative;
    width: 6rem;
    height: 6rem;
    bottom: 130rem;
    z-index: 5;
    padding: 1.314rem;
    right: 9rem;
    background-color: white;
    border-radius: 50%;
    box-shadow: 0 2rem 4rem rgba(255, 107, 0, 0.13),
      0 1rem 1rem rgba(255, 107, 0, 0.05);
  }
  &__phone {
    position: relative;
    width: 8rem;
    height: 8rem;
    bottom: 80rem;
    right: 78rem;
    z-index: 5;
    padding: 2.174rem;
    background-color: white;
    border-radius: 50%;
    box-shadow: 0 2rem 4rem rgba(255, 107, 0, 0.13),
      0 1rem 1rem rgba(255, 107, 0, 0.05);
  }
  &__gear {
    position: relative;
    width: 8.5rem;
    height: 8.5rem;
    bottom: 130rem;
    right: 50rem;
    z-index: 5;
    padding: 2.174rem;
    background-color: white;
    border-radius: 50%;
    box-shadow: 0 2rem 4rem rgba(255, 107, 0, 0.13),
      0 1rem 1rem rgba(255, 107, 0, 0.05);
  }
  &__master {
    @media (max-width: 48em) {
      width: 37.8rem;
      height: 39.6rem;
      top: -50rem;
      left: 9rem;
    }
    width: 60.9rem;
    height: 65.1rem;
    top: -80rem;
    left: 11rem;
    position: relative;
    z-index: 2;
  }
  &__line {
    @media (max-width: 48em) {
      width: 47.6rem;
      height: 46.6rem;
    }
    position: relative;
    width: 76.5rem;
    height: 76.5rem;
    z-index: 4;
  }
}
.stealth {
  z-index: 1;
}
</style>
<script>
export default {
  data() {
    return {
      isModalOpen: false,
    };
  },
};
</script>
