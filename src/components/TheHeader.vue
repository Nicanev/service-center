<template>
  <div
    class="header-menu__cover for-mobile"
    v-if="isOpenMenu"
    @click="isOpenMenu = false"
  ></div>
  <div class="header" id="header" v-if="headerActive">
    <div class="header__container">
      <img
        src="@/assets/img/Logo.svg"
        @click="scrollTo('main')"
        class="header__logo"
      />
      <ul class="header__menu">
        <li @click="scrollTo('service')"><a>Наши услуги</a></li>
        <li @click="scrollTo('about')"><a>О компании</a></li>
        <li @click="scrollTo('review')"><a>Отзывы</a></li>
        <li @click="scrollTo('orders')"><a>Выполненные заказы</a></li>
        <li @click="scrollTo('contact')"><a>Контакты</a></li>
      </ul>
    </div>
  </div>
  <div class="headerScroll" v-if="headerScrollActive">
    <div class="headerScroll__container">
      <div class="headerScroll__left">
        <img
          src="@/assets/img/Logo.svg"
          @click="scrollTo('main')"
          class="headerScroll__logo"
        />
        <ul class="headerScroll__menu">
          <li :class="{ active: active == 'main' }">
            <a @click="scrollTo('service')">Наши услуги</a>
          </li>
          <li :class="{ active: active == 'about' }">
            <a @click="scrollTo('about')">О компании</a>
          </li>
          <li :class="{ active: active == 'reviews' }">
            <a @click="scrollTo('review')">Отзывы</a>
          </li>
          <li :class="{ active: active == 'orders' }">
            <a @click="scrollTo('orders')">Выполненные заказы</a>
          </li>
          <li :class="{ active: active == 'contact' }">
            <a @click="scrollTo('contact')">Контакты</a>
          </li>
        </ul>
      </div>
      <div class="headerScroll__phone">
        <div class="headerScroll__number">
          069 82 77 38 <span>/</span> 079 92 77 38
        </div>
        <div class="headerScroll__call">
          <img src="@/assets/img/icons/phone-call.svg" />
        </div>
      </div>
    </div>
  </div>
  <div class="header-mobile for-mobile">
    <div class="header-mobile__container">
      <div class="header-mobile__left">
        <img
          src="@/assets/img/Logo.svg"
          @click="scrollTo('main')"
          alt=""
          class="header-mobile__logo"
        />
        <button class="header-mobile__menu" @click="isOpenMenu = true">
          <img src="@/assets/img/icons/menu.svg" />
        </button>
      </div>
      <div class="header-mobile__phone">
        <div class="header-mobile__number">
          069 82 77 38 <span>/</span> 079 92 77 38
        </div>
        <div class="header-mobile__call">
          <img src="@/assets/img/icons/phone-call.svg" />
        </div>
      </div>
    </div>
  </div>
  <div class="header-menu for-mobile" v-if="isOpenMenu">
    <div class="header-menu__up">
      <img src="@/assets/img/Logo.svg" />
      <button @click="isOpenMenu = false">
        <img src="@/assets/img/icons/close.svg" />
      </button>
    </div>
    <ul class="header-menu__list">
      <li><a @click="scrollTo('service')">Наши услуги</a></li>
      <li><a @click="scrollTo('about')">О компании</a></li>
      <li><a @click="scrollTo('review')">Отзывы</a></li>
      <li><a @click="scrollTo('orders')">Выполненные заказы</a></li>
      <li><a @click="scrollTo('contact')">Контакты</a></li>
    </ul>
    <div class="header-menu__address">
      <img src="@/assets/img/icons/map-pin.svg" />
      <div class="header-menu__text">
        г. Кишинев, ул. Бэнулеску Бодони, д.33
        <a href="#">Мы на карте</a>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
a {
  cursor: pointer;
}
.header-menu {
  @media (max-width: 48em) {
    display: flex !important;
  }
  position: fixed;
  top: 0;
  left: 0;
  z-index: 501;
  background-color: #f4f9fc;
  height: 100vh;
  width: 37rem;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  &__cover {
    position: absolute;
    z-index: 400;
    height: 200vh;
    background: #dce0e2;
    opacity: 0.9;
    width: 100%;
  }
  &__text {
    display: flex;
    flex-direction: column;
    font-size: 1.6rem;
    color: #13171d;
    width: 20rem;
    a {
      text-decoration-line: underline;
      color: #015aa9;
    }
  }
  &__address {
    display: flex;
    gap: 0.7rem;
    padding-left: 2.4rem;
    img {
      width: 3.2rem;
      height: 3.2rem;
    }
  }
  &__list {
    padding-left: 2.4rem;
    font-size: 2rem;
    display: flex;
    flex-direction: column;
    gap: 4rem;
    a {
      font-weight: 600;
      color: #13171d;
    }
  }
  &__up {
    display: flex;
    gap: 4.5rem;
    align-items: center;
    button {
      display: flex;
      align-items: center;
      justify-content: center;
      width: 4.8rem;
      height: 4.8rem;
      border-radius: 1.5rem;
      background-color: white;
      border: none;
      box-shadow: 0px 8px 16px rgba(255, 107, 0, 0.16);
    }
    img {
      width: 20rem;
      height: 7.8rem;
    }
  }
}
.header-mobile {
  &__container {
    display: flex;
    justify-content: space-between;
  }
  &__left {
    display: flex;
    gap: 4rem;
    align-items: center;
  }
  &__logo {
    width: 20rem;
    height: 7.8rem;
  }
  &__phone {
    display: flex;
    gap: 2rem;
    align-items: center;
  }
  &__call {
    cursor: pointer;
    padding: 1.6rem;
    background-color: rgba(226, 0, 26, 0.1);
    border-radius: 1.5rem;
    img {
      width: 1.6rem;
      height: 1.6rem;
    }
  }

  &__menu {
    width: 4.8rem;
    height: 4.8rem;
    border-radius: 1.5rem;
    background-color: white;
    border: none;
    box-shadow: 0px 8px 16px rgba(255, 107, 0, 0.16);
  }
  &__number {
    color: #13171d;
    font-size: 1.4rem;
    font-weight: 600;
    span {
      color: black;
      opacity: 0.2;
    }
  }
}
.active {
  padding-bottom: 2rem;
  border-bottom: 0.2rem solid #e2001a;
  a {
    color: #e2001a;
  }
}
.headerScroll {
  @media (max-width: 48em) {
    display: none;
  }
  position: fixed;
  z-index: 100;
  background-color: #f4f9fc;
  box-shadow: 0px 5px 20px #cddae1;
  width: 100%;
  &__phone {
    display: flex;
    gap: 3.5rem;
    align-items: center;
  }
  &__call {
    cursor: pointer;
    padding: 1.6rem;
    background-color: rgba(226, 0, 26, 0.1);
    border-radius: 1.5rem;
    img {
      width: 1.6rem;
      height: 1.6rem;
    }
  }
  &__number {
    color: #13171d;
    font-size: 2rem;
    font-weight: 600;
    span {
      color: black;
      opacity: 0.2;
    }
  }
  &__container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    // height: 8rem;
  }
  &__left {
    display: flex;
    gap: 13rem;
  }
  &__logo {
    width: 14.5rem;
    height: 5rem;
  }
  &__menu {
    display: flex;
    padding-top: 3rem;
    gap: 2.4rem;
    a {
      font-size: 1.6rem;
      font-weight: 600;
      color: --main-font-color;
    }
  }
}
.header {
  @media (max-width: 48em) {
    display: none;
  }
  &__container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 12.5rem;
  }
  &__logo {
    width: 20.2rem;
    height: 7.2rem;
  }
  &__menu {
    display: flex;
    gap: 2.4rem;
    a {
      font-size: 1.6rem;
      font-weight: 600;
      color: --main-font-color;
    }
  }
}
</style>

<script>
export default {
  data() {
    return {
      headerScrollActive: false,
      headerActive: true,
      active: "main",
      isOpenMenu: false,
    };
  },
  methods: {
    scrollTo(name) {
      if (name == "main") {
        window.scrollTo(0, 0);
      }
      if (name == "about") {
        window.scrollTo(0, 2000);
      }
      if (name == "service") {
        window.scrollTo(0, 1200);
      }
      if (name == "review") {
        window.scrollTo(0, 2600);
      }
      if (name == "orders") {
        window.scrollTo(0, 3300);
      }
      if (name == "contact") {
        window.scrollTo(0, 6575);
      }
    },
  },
  mounted() {
    const header = document.getElementById("header");
    const headerHeight = header.offsetHeight;
    window.addEventListener("scroll", () => {
      let scroll = window.scrollY;
      if (scroll >= headerHeight + 550) {
        this.headerActive = false;
      } else {
        this.headerActive = true;
      }
      if (scroll >= headerHeight + 750) {
        this.headerScrollActive = true;
      } else {
        this.headerScrollActive = false;
      }
      if (scroll >= 1900 && scroll <= 2500) {
        this.active = "about";
      } else if (scroll >= 2500 && scroll <= 2900) {
        this.active = "reviews";
      } else if (scroll >= 2900 && scroll <= 6475) {
        this.active = "orders";
      } else if (scroll >= 6475) {
        this.active = "contact";
      } else {
        this.active = "main";
      }
    });
  },
};
</script>
