<template>
  <section class="service">
    <div class="service__container">
      <div class="service__title">Мы работаем с устройствами:</div>
      <div class="service__card">
        <img src="@/assets/img/services/Apple.png" />
        <p>Apple</p>
        <button></button>
      </div>
      <div class="service__card">
        <img src="@/assets/img/services/Android.png" />
        <p>Android</p>
        <button></button>
      </div>
      <div class="service__card">
        <img src="@/assets/img/services/Gadgets.png" />
        <p>Гаджетами</p>
        <button></button>
      </div>
      <div class="service__card">
        <img src="@/assets/img/services/laptop.png" />
        <p>Ноутбуками</p>
        <button></button>
      </div>
      <div class="service__card">
        <img src="@/assets/img/services/PC.png" />
        <p>Моноблоками и PC</p>
        <button></button>
      </div>
      <div class="service__card">
        <img src="@/assets/img/services/assecsories.png" />
        <p>Другими устройствами</p>
        <button></button>
      </div>
    </div>
  </section>
</template>

<style lang="scss">
.service {
  margin-bottom: 8rem;
  &__container {
    @media (max-width: 48em) {
      max-width: 100%;
      padding: 0 0;
    }
    display: flex;
    flex-wrap: wrap;
    gap: 3.2rem;
    max-width: 130.4rem;
  }
  &__title {
    @media (max-width: 48em) {
      font-size: 4rem;
      margin-bottom: 4rem;
      text-align: center;
    }
    font-family: "Bebas Neue", sans-serif;
    color: #13171d;
    font-size: 8rem;
    max-width: 60rem;
  }
  &__card {
    position: relative;
    margin-bottom: 3.5rem;
    width: 30.2rem;
    background-color: rgba(255, 255, 255, 0.507);
    border-radius: 3rem;
    box-shadow: 0px 50px 60px rgba(255, 107, 0, 0.08),
      0px 8px 10px rgba(255, 107, 0, 0.08);
    // background-size: cover;
    // background-size: contain;
    height: 31rem;
    // background-image: url("../assets/img/backgrounds/card.svg");
    // background-clip: border-box;
    // background-position: center;
    button {
      position: absolute;
      bottom: 0rem;
      right: 1rem;
      background-image: url("../assets/img/icons/Arrow.svg");
      background-repeat: no-repeat;
      border-radius: 50%;
      border: none;
      background-size: 2.4rem 2.4rem;
      background-color: white;
      padding: 1.5rem;
      background-position: center;
      height: 2.4rem;
      width: 2.4rem;
      box-shadow: 0px 20px 40px rgba(255, 107, 0, 0.13),
        0px 10px 10px rgba(255, 107, 0, 0.05);
      outline: 1.2rem solid rgba(255, 255, 255, 0.493);
      cursor: pointer;
    }
    img {
      position: absolute;
      bottom: 12rem;
      left: 5rem;
      max-width: 25rem;
      max-height: 24rem;
    }
    p {
      position: absolute;
      bottom: 5rem;
      color: #13171d;
      font-size: 2.2rem;
      font-weight: bold;
      left: 3rem;
    }
  }
}
</style>
