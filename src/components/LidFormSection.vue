<template>
  <section class="lid">
    <div class="lid__container">
      <div class="lid__body">
        <div class="lid__text">
          <div class="lid__percent">50%</div>
          <div class="lid__title">
            Записаться на диагностику в <span>удобное</span> вам время
          </div>
        </div>
        <form class="lid__form">
          <input type="text" placeholder="День" required />
          <input type="text" placeholder="Время" class="time" required />
          <input type="tel" placeholder="Телефон" required />
          <button>Записаться</button>
        </form>
      </div>
    </div>
  </section>
</template>

<style lang="scss">
.lid {
  margin-bottom: 11rem;
  &__body {
    width: 130rem;
    margin: 0 auto;
    border-radius: 3rem;
    border: 0.1rem solid #c7d1d7;
    display: flex;
    justify-content: space-between;
    padding: 0 11rem;
    padding-bottom: 3rem;
    @media (max-width: 48em) {
      flex-direction: column;
    }
  }
  &__title {
    margin-top: -5rem;
    font-size: 4.8rem;
    font-family: "Bebas Neue", sans-serif;
    color: #13171d;
    max-width: 37.7rem;
    span {
      color: #e2001a;
    }
  }
  &__form {
    margin-top: 4.7rem;
    display: flex;
    flex-wrap: wrap;
    gap: 2.5rem;
    width: 53rem;
    .time {
      width: 26rem;
    }
    input {
      color: #646464;
      height: 6.4rem;
      width: 24rem;
      text-indent: 2.4rem;
      font-size: 1.4rem;
      border: 0.1rem solid #dadada;
      border-radius: 1.5rem;
      background-color: transparent;
    }
    input[type="tel"] {
      width: 100%;
    }
    button {
      background: #e2001a;
      color: white;
      border-radius: 1.5rem;
      font-size: 1.6rem;
      font-weight: 600;
      border: none;
      padding: 1.8rem 7.1rem;
      cursor: pointer;
    }
  }
  &__percent {
    color: #ff6b00;
    position: relative;
    max-width: max-content;
    bottom: 5rem;
    font-family: "Bebas Neue", sans-serif;
    background-color: #f4f9fc;
    font-size: 11.3rem;
    text-shadow: 0px 100px 80px rgba(255, 107, 0, 0.11),
      0px 46.233px 36.9864px rgba(255, 107, 0, 0.0815843),
      0px 26.4535px 21.1628px rgba(255, 107, 0, 0.0689459),
      0px 16.0571px 12.8457px rgba(255, 107, 0, 0.0593943),
      0px 9.67509px 7.74008px rgba(255, 107, 0, 0.0506057),
      0px 5.38772px 4.31018px rgba(255, 107, 0, 0.0410541),
      0px 2.31722px 1.85378px rgba(255, 107, 0, 0.0284157);
  }
}
</style>
