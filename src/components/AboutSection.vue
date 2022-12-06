<template>
  <section class="about" id="about">
    <div class="about__container">
      <div class="about__des">
        <div class="about__title">О компании Arron</div>
        <div class="about__subtitle">
          Узнайте о нашей компании больше из видео за 1 минуту.
        </div>
        <button class="about__btn">
          Смотреть
          <img src="@/assets/img/about/Arrow.svg" />
        </button>
      </div>
      <div class="about__cards">
        <div class="about__card">
          <img src="@/assets/img/hero/adv1.svg" />
          <h1>Выезжаем в любую точку Кишинева</h1>
          <p></p>
        </div>
        <div class="about__card">
          <img src="@/assets/img/icons/trusted.svg" />
          <h1>Работы от 30 минут</h1>
          <p>
            Время работы или настройки занимает от 30 минут до несколько часов.
          </p>
        </div>
        <div class="about__card">
          <img src="@/assets/img/icons/payment.svg" />
          <h1>Удобный способ оплаты</h1>
          <p>Оплата наличными или по перечеслению компаниям.</p>
        </div>
        <div class="about__card">
          <img src="@/assets/img/icons/secure.svg" />
          <h1>Гарантия на все выполненые услуги</h1>
          <p>
            Запчасти, фотографии и сообщения под Вашим контролем. После работ
            инженер отдаст Вам старые запчасти.
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss">
.about {
  margin-bottom: 12rem;
  padding: 8rem 7rem;
  background: linear-gradient(180deg, #ebf3f8 0%, rgba(235, 243, 248, 0) 100%);
  &__container {
    @media (max-width: 48em) {
      flex-direction: column;
    }
    display: flex;
    gap: 10rem;
  }
  &__title {
    color: #13171d;
    font-size: 8rem;
    max-width: 54.2rem;
    font-family: "Bebas Neue", sans-serif;
  }
  &__subtitle {
    color: #444444;
    font-size: 2.4rem;
    max-width: 52.7rem;
  }
  &__cards {
    display: flex;
    width: 75rem;
    flex-wrap: wrap;
    justify-content: space-between;
  }
  &__card {
    img {
      width: 8rem;
      height: 8rem;
    }
    h1 {
      color: #13171d;
      font-size: 2rem;
      font-weight: 600;
      margin-bottom: 1.6rem;
    }
    p {
      color: #444444;
      font-size: 1.8rem;
      width: 33.6rem;
    }
  }
  &__btn {
    display: flex;
    align-items: center;
    gap: 1.6rem;
    background-color: #e2001a;
    border-radius: 1.5rem;
    border: none;
    padding: 1.8rem 8rem;
    color: white;
    font-size: 1.6rem;
    font-weight: 600;
    margin-top: 9rem;
    cursor: pointer;
    img {
      width: 2.4rem;
      height: 2.4rem;
    }
  }
}
</style>
