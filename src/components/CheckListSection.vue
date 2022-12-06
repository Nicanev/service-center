<template>
  <section class="checklist">
    <div class="checklist__container">
      <div class="checklist__des">
        <div class="checklist__title">
          Что делать если ноутбук или телефон медлено работает
        </div>
        <div class="checklist__subtitle">
          <img src="@/assets/img/icons/checklist.svg" />
          <p>
            Получите чек лист - Что делать, если ноутбук или телефон грузится
          </p>
        </div>
        <button class="checklist__btn">Получить чек лист</button>
      </div>
      <div class="checklist__service">
        <div class="checklist__title">Наши услуги</div>
        <div class="checklist__lists">
          <ul>
            <li>ремонт ноутбуков</li>
            <li>ремонт смартфонов</li>
            <li>заправка и ремонт картриджей</li>
            <li>установка СНПЧ</li>
            <li>ремонт компьютеров</li>
            <li>ремонт компьютеров</li>
          </ul>
          <ul>
            <li>ремонт планшетов</li>
            <li>ремонт КПК</li>
            <li>ремонт мониторов</li>
            <li>ремонт принтеров</li>
            <li>ремонт роутеров</li>
            <li>восстановление жестких дисков</li>
            <li>компьютерная помощь и IT аутсорсинги др.</li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss">
.checklist {
  margin-bottom: 6rem;
  &__container {
    display: flex;
    gap: 10rem;
    @media (max-width: 48em) {
      flex-direction: column;
    }
  }
  &__lists {
    margin-top: 2rem;
    display: flex;
    gap: 4rem;
    li {
      color: #444444;
      font-size: 1.8rem;
      margin-bottom: 1.8rem;
    }
    ul li::before {
      content: "\2022";
      color: #e2001a;
      font-weight: bold;
      display: inline-block;
      width: 1em;
      margin-left: -1em;
    }
  }
  &__title {
    color: #13171d;
    font-size: 4.8rem;
    max-width: 42.7rem;
  }
  &__subtitle {
    margin-top: 2rem;
    display: flex;
    gap: 0.8rem;
    align-items: center;
    p {
      font-size: 1.4rem;
      max-width: 28.8rem;
    }
  }
  &__btn {
    margin-top: 4rem;
    color: white;
    background-color: #e2001a;
    border: none;
    border-radius: 1.5rem;
    padding: 2.5rem 4rem;
    font-size: 1.6rem;
    font-weight: 600;
    cursor: pointer;
  }
}
</style>
