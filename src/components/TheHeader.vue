<template>
  <div class="header" id="header" v-if="headerActive">
    <div class="header__container">
      <img src="@/assets/img/Logo.svg" class="header__logo" />
      <ul class="header__menu">
        <li><a href="#">Наши услуги</a></li>
        <li><a href="#">О компании</a></li>
        <li><a href="#">Отзывы</a></li>
        <li><a href="#">Выполненные заказы</a></li>
        <li><a href="#">Контакты</a></li>
      </ul>
    </div>
  </div>
  <div class="headerScroll" v-if="headerScrollActive">
    <div class="headerScroll__container">
      <div class="headerScroll__left">
        <img src="@/assets/img/Logo.svg" class="headerScroll__logo" />
        <ul class="headerScroll__menu">
          <li :class="{ active: active == 'main' }">
            <a href="#">Наши услуги</a>
          </li>
          <li :class="{ active: active == 'about' }">
            <a href="#">О компании</a>
          </li>
          <li :class="{ active: active == 'reviews' }">
            <a href="#">Отзывы</a>
          </li>
          <li :class="{ active: active == 'orders' }">
            <a href="#">Выполненные заказы</a>
          </li>
          <li :class="{ active: active == 'contact' }">
            <a href="#">Контакты</a>
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
</template>

<style lang="scss">
.active {
  padding-bottom: 2rem;
  border-bottom: 0.2rem solid #e2001a;
  a {
    color: #e2001a;
  }
}
.headerScroll {
  position: fixed;
  z-index: 100;
  background-color: #f4f9fc;
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
    @media (max-width: 48em) {
      display: none;
    }
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
    };
  },
  methods: {
    onScroll() {
      console.log("scroll");
    },
  },
  mounted() {
    const header = document.getElementById("header");
    const headerHeight = header.offsetHeight;
    console.log(headerHeight);
    window.addEventListener("scroll", () => {
      let scroll = window.scrollY;
      if (scroll >= headerHeight + 80) {
        this.headerActive = false;
      } else {
        this.headerActive = true;
      }
      if (scroll >= headerHeight + 400) {
        this.headerScrollActive = true;
      } else {
        this.headerScrollActive = false;
      }
      if (scroll >= 1900 && scroll <= 2500) {
        this.active = "about";
      } else if (scroll >= 2500 && scroll <= 2900) {
        this.active = "reviews";
      } else if (scroll >= 2900) {
        this.active = "orders";
      } else {
        this.active = "main";
      }
    });
  },
};
</script>
