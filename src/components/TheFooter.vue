<template>
  <footer class="footer">
    <div class="footer__container">
      <div class="footer__main">
        <div class="footer__connect">
          <div class="footer__connect-icon">
            <img src="@/assets/img/icons/tel.svg" />
            <p>069 82 77 38079 92 77 38</p>
          </div>
          <div class="footer__connect-icon">
            <img src="@/assets/img/icons/email.svg" />
            <p>info@arron.md</p>
          </div>
          <div class="footer__connect-icon">
            <img src="@/assets/img/icons/location.svg" />
            <p>г. Кишинев, ул. Бэнулеску Бодони, д.33</p>
          </div>
        </div>
        <div class="footer__down">
          <div class="footer__rate">
            <h1>Рейтинг сервиса</h1>
            <img src="@/assets/img/icons/Stars.svg" />
            <p>4.8/5.0 - 403 голоса</p>
          </div>
          <div class="footer__social">
            <h1>Мы в соцсетях</h1>
            <div class="footer__social-icons">
              <img src="@/assets/img/icons/instagram.svg" />
              <img src="@/assets/img/icons/facebook.svg" />
              <img src="@/assets/img/icons/tiktok.svg" />
              <img src="@/assets/img/icons/youtube.svg" />
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="footer__map"></div>
  </footer>
</template>

<style lang="scss">
.footer {
  margin-top: 6rem;
  &__connect-icon {
    display: flex;
    align-items: center;
    flex-direction: column;
    gap: 1.6rem;
    p {
      max-width: 15rem;
      font-weight: 500;
      color: #13171d;
      font-size: 1.8rem;
      text-align: center;
    }
  }
  &__map {
    position: relative;
    margin-top: -8rem;
    z-index: 1;
    background-image: url("../assets/img/backgrounds/Map.png");
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    width: 100%;
    height: 75rem;
  }
  &__main {
    @media (max-width: 48em) {
      width: 60rem;
    }
    position: relative;
    z-index: 2;
    width: 130rem;
    background-color: white;
    border-radius: 3rem;
    margin: 0 auto;
    padding: 5rem 7rem;
    box-shadow: 0px 50px 60px rgba(255, 107, 0, 0.08),
      0px 8px 10px rgba(255, 107, 0, 0.08);
  }
  &__down {
    @media (max-width: 48em) {
      gap: 10rem;
    }
    display: flex;
    gap: 19rem;
  }
  &__social {
    display: flex;
    flex-direction: column;
    gap: 1.4rem;
    h1 {
      font-size: 2rem;
      font-weight: 600;
      color: #13171d;
    }
  }
  &__social-icons {
    display: flex;
    gap: 1.5rem;
    img {
      width: 3.5rem;
      height: 3.5rem;
      cursor: pointer;
    }
  }
  &__rate {
    display: flex;
    flex-direction: column;
    gap: 1rem;
    h1 {
      font-size: 2rem;
      font-weight: 600;
      color: #13171d;
    }
    p {
      font-size: 1.8rem;
      color: #444444;
    }
    img {
      width: 19.2rem;
      height: 3.6rem;
    }
  }
  &__connect {
    margin-bottom: 3rem;
    display: flex;
    gap: 5rem;
    img {
      width: 5.6rem;
      height: 5.6rem;
      cursor: pointer;
    }
  }
}
</style>
