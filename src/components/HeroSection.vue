<template>
  <section class="hero" id="hero">
    <div class="consult" v-if="isModalOpen">
      <div class="consult__cover" @click="isModalOpen = false"></div>
      <div class="consult__body" v-if="!isRequestSend">
        <button class="consult__close" @click="isModalOpen = false">
          <svg
            viewBox="0 0 24 25"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M6 19L18.7279 6.27208"
              stroke="#C6C6C6"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
            <path
              d="M6 6L18.7279 18.7279"
              stroke="#C6C6C6"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
          </svg>
        </button>
        <div class="consult__title">
          Оставьте заявку на <span>бесплатную</span> консультацию
        </div>
        <form onsubmit="return false;" class="consult__form">
          <input type="text" placeholder="Имя" required />
          <input type="text" placeholder="Телефон" required />
          <button @click="isRequestSend = true">Получить консультацию</button>
        </form>
      </div>
      <div class="consult__body" v-if="isRequestSend">
        <button class="consult__close" @click="isModalOpen = false">
          <svg
            viewBox="0 0 24 25"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M6 19L18.7279 6.27208"
              stroke="#C6C6C6"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
            <path
              d="M6 6L18.7279 18.7279"
              stroke="#C6C6C6"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
          </svg>
        </button>
        <div class="consult__img"></div>
        <div class="consult__title">Ваша заявка отправлена</div>
        <div class="consult__subtitle">
          Мы свяжемся с вами в ближайшее время
        </div>
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
              <div class="stock__percent">
                50%
                <svg
                  viewBox="0 0 185 213"
                  fill="none"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <g filter="url(#filter0_dddddd_3_648)">
                    <path
                      d="M104.089 19.028C103.723 14.2556 101.501 11.2649 99.5406 8.62578C97.7255 6.18254 96.1578 4.07266 96.1578 0.960289C96.1578 0.710289 96.0178 0.481789 95.7958 0.367226C95.5731 0.251977 95.3056 0.270852 95.1031 0.417976C92.1591 2.5246 89.7028 6.07516 88.8447 9.46291C88.249 11.8215 88.1702 14.473 88.1591 16.2242C85.4404 15.6435 84.8245 11.5767 84.818 11.5324C84.7874 11.3215 84.6585 11.1379 84.471 11.0377C84.2816 10.9387 84.0589 10.9315 83.8668 11.0266C83.7243 11.0956 80.3675 12.8012 80.1721 19.6113C80.1585 19.8378 80.1578 20.0651 80.1578 20.2923C80.1578 26.9083 85.5413 32.2915 92.1578 32.2915C92.167 32.2921 92.1767 32.2934 92.1845 32.2915C92.1871 32.2915 92.1897 32.2915 92.193 32.2915C98.7933 32.2725 104.158 26.8967 104.158 20.2923C104.158 19.9596 104.089 19.028 104.089 19.028Z"
                      fill="#FF6B00"
                    />
                  </g>
                  <path
                    d="M92.1578 30.7925C88.8492 30.7925 86.1579 27.9166 86.1579 24.3814C86.1579 24.2609 86.1569 24.1394 86.1656 23.9906C86.2057 22.4997 86.488 21.482 86.7975 20.805C87.3776 22.055 88.4147 23.204 90.0992 23.204C90.652 23.204 91.0992 22.7553 91.0992 22.2009C91.0992 20.7728 91.1286 19.1252 91.483 17.6382C91.7985 16.3197 92.5523 14.9169 93.5074 13.7925C93.9322 15.252 94.7604 16.4333 95.569 17.5863C96.7262 19.2358 97.9224 20.9412 98.1324 23.8495C98.1451 24.0219 98.1578 24.1953 98.1578 24.3814C98.1576 27.9165 95.4663 30.7925 92.1578 30.7925Z"
                    fill="#FFD66B"
                  />
                  <defs>
                    <filter
                      id="filter0_dddddd_3_648"
                      x="0.157837"
                      y="0.29248"
                      width="184"
                      height="212"
                      filterUnits="userSpaceOnUse"
                      color-interpolation-filters="sRGB"
                    >
                      <feFlood flood-opacity="0" result="BackgroundImageFix" />
                      <feColorMatrix
                        in="SourceAlpha"
                        type="matrix"
                        values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0"
                        result="hardAlpha"
                      />
                      <feOffset dy="2.76726" />
                      <feGaussianBlur stdDeviation="1.1069" />
                      <feColorMatrix
                        type="matrix"
                        values="0 0 0 0 1 0 0 0 0 0.419608 0 0 0 0 0 0 0 0 0.0477948 0"
                      />
                      <feBlend
                        mode="normal"
                        in2="BackgroundImageFix"
                        result="effect1_dropShadow_3_648"
                      />
                      <feColorMatrix
                        in="SourceAlpha"
                        type="matrix"
                        values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0"
                        result="hardAlpha"
                      />
                      <feOffset dy="6.6501" />
                      <feGaussianBlur stdDeviation="2.66004" />
                      <feColorMatrix
                        type="matrix"
                        values="0 0 0 0 1 0 0 0 0 0.419608 0 0 0 0 0 0 0 0 0.0686618 0"
                      />
                      <feBlend
                        mode="normal"
                        in2="effect1_dropShadow_3_648"
                        result="effect2_dropShadow_3_648"
                      />
                      <feColorMatrix
                        in="SourceAlpha"
                        type="matrix"
                        values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0"
                        result="hardAlpha"
                      />
                      <feOffset dy="12.5216" />
                      <feGaussianBlur stdDeviation="5.00862" />
                      <feColorMatrix
                        type="matrix"
                        values="0 0 0 0 1 0 0 0 0 0.419608 0 0 0 0 0 0 0 0 0.085 0"
                      />
                      <feBlend
                        mode="normal"
                        in2="effect2_dropShadow_3_648"
                        result="effect3_dropShadow_3_648"
                      />
                      <feColorMatrix
                        in="SourceAlpha"
                        type="matrix"
                        values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0"
                        result="hardAlpha"
                      />
                      <feOffset dy="22.3363" />
                      <feGaussianBlur stdDeviation="8.93452" />
                      <feColorMatrix
                        type="matrix"
                        values="0 0 0 0 1 0 0 0 0 0.419608 0 0 0 0 0 0 0 0 0.101338 0"
                      />
                      <feBlend
                        mode="normal"
                        in2="effect3_dropShadow_3_648"
                        result="effect4_dropShadow_3_648"
                      />
                      <feColorMatrix
                        in="SourceAlpha"
                        type="matrix"
                        values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0"
                        result="hardAlpha"
                      />
                      <feOffset dy="41.7776" />
                      <feGaussianBlur stdDeviation="16.711" />
                      <feColorMatrix
                        type="matrix"
                        values="0 0 0 0 1 0 0 0 0 0.419608 0 0 0 0 0 0 0 0 0.122205 0"
                      />
                      <feBlend
                        mode="normal"
                        in2="effect4_dropShadow_3_648"
                        result="effect5_dropShadow_3_648"
                      />
                      <feColorMatrix
                        in="SourceAlpha"
                        type="matrix"
                        values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0"
                        result="hardAlpha"
                      />
                      <feOffset dy="100" />
                      <feGaussianBlur stdDeviation="40" />
                      <feColorMatrix
                        type="matrix"
                        values="0 0 0 0 1 0 0 0 0 0.419608 0 0 0 0 0 0 0 0 0.17 0"
                      />
                      <feBlend
                        mode="normal"
                        in2="effect5_dropShadow_3_648"
                        result="effect6_dropShadow_3_648"
                      />
                      <feBlend
                        mode="normal"
                        in="SourceGraphic"
                        in2="effect6_dropShadow_3_648"
                        result="shape"
                      />
                    </filter>
                  </defs>
                </svg>
              </div>
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
      <div class="hero__stock-mobile stock-mobile for-mobile">
        <div class="stock-mobile__container">
          <div class="stock-mobile__body">
            <div class="stock-mobile__percent">
              50%
              <svg
                viewBox="0 0 185 213"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <g filter="url(#filter0_dddddd_3_648)">
                  <path
                    d="M104.089 19.028C103.723 14.2556 101.501 11.2649 99.5406 8.62578C97.7255 6.18254 96.1578 4.07266 96.1578 0.960289C96.1578 0.710289 96.0178 0.481789 95.7958 0.367226C95.5731 0.251977 95.3056 0.270852 95.1031 0.417976C92.1591 2.5246 89.7028 6.07516 88.8447 9.46291C88.249 11.8215 88.1702 14.473 88.1591 16.2242C85.4404 15.6435 84.8245 11.5767 84.818 11.5324C84.7874 11.3215 84.6585 11.1379 84.471 11.0377C84.2816 10.9387 84.0589 10.9315 83.8668 11.0266C83.7243 11.0956 80.3675 12.8012 80.1721 19.6113C80.1585 19.8378 80.1578 20.0651 80.1578 20.2923C80.1578 26.9083 85.5413 32.2915 92.1578 32.2915C92.167 32.2921 92.1767 32.2934 92.1845 32.2915C92.1871 32.2915 92.1897 32.2915 92.193 32.2915C98.7933 32.2725 104.158 26.8967 104.158 20.2923C104.158 19.9596 104.089 19.028 104.089 19.028Z"
                    fill="#FF6B00"
                  />
                </g>
                <path
                  d="M92.1578 30.7925C88.8492 30.7925 86.1579 27.9166 86.1579 24.3814C86.1579 24.2609 86.1569 24.1394 86.1656 23.9906C86.2057 22.4997 86.488 21.482 86.7975 20.805C87.3776 22.055 88.4147 23.204 90.0992 23.204C90.652 23.204 91.0992 22.7553 91.0992 22.2009C91.0992 20.7728 91.1286 19.1252 91.483 17.6382C91.7985 16.3197 92.5523 14.9169 93.5074 13.7925C93.9322 15.252 94.7604 16.4333 95.569 17.5863C96.7262 19.2358 97.9224 20.9412 98.1324 23.8495C98.1451 24.0219 98.1578 24.1953 98.1578 24.3814C98.1576 27.9165 95.4663 30.7925 92.1578 30.7925Z"
                  fill="#FFD66B"
                />
                <defs>
                  <filter
                    id="filter0_dddddd_3_648"
                    x="0.157837"
                    y="0.29248"
                    width="184"
                    height="212"
                    filterUnits="userSpaceOnUse"
                    color-interpolation-filters="sRGB"
                  >
                    <feFlood flood-opacity="0" result="BackgroundImageFix" />
                    <feColorMatrix
                      in="SourceAlpha"
                      type="matrix"
                      values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0"
                      result="hardAlpha"
                    />
                    <feOffset dy="2.76726" />
                    <feGaussianBlur stdDeviation="1.1069" />
                    <feColorMatrix
                      type="matrix"
                      values="0 0 0 0 1 0 0 0 0 0.419608 0 0 0 0 0 0 0 0 0.0477948 0"
                    />
                    <feBlend
                      mode="normal"
                      in2="BackgroundImageFix"
                      result="effect1_dropShadow_3_648"
                    />
                    <feColorMatrix
                      in="SourceAlpha"
                      type="matrix"
                      values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0"
                      result="hardAlpha"
                    />
                    <feOffset dy="6.6501" />
                    <feGaussianBlur stdDeviation="2.66004" />
                    <feColorMatrix
                      type="matrix"
                      values="0 0 0 0 1 0 0 0 0 0.419608 0 0 0 0 0 0 0 0 0.0686618 0"
                    />
                    <feBlend
                      mode="normal"
                      in2="effect1_dropShadow_3_648"
                      result="effect2_dropShadow_3_648"
                    />
                    <feColorMatrix
                      in="SourceAlpha"
                      type="matrix"
                      values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0"
                      result="hardAlpha"
                    />
                    <feOffset dy="12.5216" />
                    <feGaussianBlur stdDeviation="5.00862" />
                    <feColorMatrix
                      type="matrix"
                      values="0 0 0 0 1 0 0 0 0 0.419608 0 0 0 0 0 0 0 0 0.085 0"
                    />
                    <feBlend
                      mode="normal"
                      in2="effect2_dropShadow_3_648"
                      result="effect3_dropShadow_3_648"
                    />
                    <feColorMatrix
                      in="SourceAlpha"
                      type="matrix"
                      values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0"
                      result="hardAlpha"
                    />
                    <feOffset dy="22.3363" />
                    <feGaussianBlur stdDeviation="8.93452" />
                    <feColorMatrix
                      type="matrix"
                      values="0 0 0 0 1 0 0 0 0 0.419608 0 0 0 0 0 0 0 0 0.101338 0"
                    />
                    <feBlend
                      mode="normal"
                      in2="effect3_dropShadow_3_648"
                      result="effect4_dropShadow_3_648"
                    />
                    <feColorMatrix
                      in="SourceAlpha"
                      type="matrix"
                      values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0"
                      result="hardAlpha"
                    />
                    <feOffset dy="41.7776" />
                    <feGaussianBlur stdDeviation="16.711" />
                    <feColorMatrix
                      type="matrix"
                      values="0 0 0 0 1 0 0 0 0 0.419608 0 0 0 0 0 0 0 0 0.122205 0"
                    />
                    <feBlend
                      mode="normal"
                      in2="effect4_dropShadow_3_648"
                      result="effect5_dropShadow_3_648"
                    />
                    <feColorMatrix
                      in="SourceAlpha"
                      type="matrix"
                      values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0"
                      result="hardAlpha"
                    />
                    <feOffset dy="100" />
                    <feGaussianBlur stdDeviation="40" />
                    <feColorMatrix
                      type="matrix"
                      values="0 0 0 0 1 0 0 0 0 0.419608 0 0 0 0 0 0 0 0 0.17 0"
                    />
                    <feBlend
                      mode="normal"
                      in2="effect5_dropShadow_3_648"
                      result="effect6_dropShadow_3_648"
                    />
                    <feBlend
                      mode="normal"
                      in="SourceGraphic"
                      in2="effect6_dropShadow_3_648"
                      result="shape"
                    />
                  </filter>
                </defs>
              </svg>
            </div>
            <div class="stock-mobile__text">
              <div class="stock-mobile__title">
                скидка на ремонт телефонов, ноутбуков и планшетов до
                <span>-50%</span>
              </div>
              <div class="stock-mobile__end">
                <h1>Конец акции:</h1>
                <div class="stock-mobile__time">
                  <div class="stock-mobile__clock">
                    <span>2</span> <span>:</span> <span>18</span> <span>:</span>
                    <span>56</span>
                  </div>
                  <div class="stock-mobile__designations">
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
          <p>Выезд курьера Буюканы Чеканы, Рышкановка, центр, Ботаника.</p>
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
  height: 70%;
  display: flex;
  align-items: center;
  justify-content: center;
  &__close {
    background-color: transparent;
    border: none;
    position: absolute;
    right: 2.6rem;
    top: 2.6rem;
    svg {
      width: 2.4rem;
      height: 2.4rem;
    }
    &:hover {
      path {
        stroke: #8a8989;
      }
    }
  }
  &__subtitle {
    margin: 0 auto;
    font-size: 1.8rem;
    color: #13171d;
  }
  &__img {
    margin: 0 auto;
    margin-bottom: 4rem;
    width: 3.3rem;
    height: 2.2rem;
    background-image: url("../assets/img/icons/check.svg");
    background-position: center;
    background-repeat: no-repeat;
    background-color: #ffd66b;
    box-shadow: 0px 30px 40px rgba(255, 214, 107, 0.5);
    padding: 3.2rem 2.8rem;
    border-radius: 50%;
  }
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
  &__form {
    display: flex;
    flex-direction: column;
    gap: 2rem;
    input {
      color: #646464;
      height: 6.4rem;
      width: 42rem;
      text-indent: 2.4rem;
      font-size: 1.4rem;
      border: 0.1rem solid #dadada;
      border-radius: 1.5rem;
      background-color: transparent;
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
      &:hover {
        background-color: #fc142f;
        transition: 0.2s;
      }
      &:active {
        box-shadow: inset 0px 3px 0px #d10018;
      }
    }
  }
  &__title {
    font-family: "Bebas Neue", sans-serif;
    font-size: 3.2rem;
    text-align: center;
    max-width: 32.5rem;
    margin: 0 auto;
    margin-bottom: 2rem;
    span {
      color: #e2001a;
    }
  }
}
.stock-mobile {
  margin-bottom: 6rem;
  &__container {
    padding: 0 0rem;
  }
  &__body {
    background-color: white;
    display: flex;
    gap: 6rem;
    width: 100%;
    height: 20rem;
    margin: 0 auto;
    padding: 3rem 5rem;
    border-radius: 3rem;
    box-shadow: 0px 7.1rem 8rem rgba(255, 107, 0, 0.11),
      0px 2.14044rem 2.41177rem rgba(255, 107, 0, 0.0716748),
      0px 0.88903rem 1.00172rem rgba(255, 107, 0, 0.055),
      0px 0.321545rem 0.362304rem rgba(255, 107, 0, 0.0383252);
  }
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
  &__title {
    color: #13171d;
    font-size: 2rem;
    width: 32rem;
    span {
      font-weight: bold;
    }
  }
  &__end {
    margin-top: 1.2rem;
    h1 {
      color: #13171d;
      font-weight: 600;
      font-size: 2rem;
      opacity: 0.5;
    }
  }
  &__percent {
    color: #ff6b00;
    font-size: 11.3rem;
    font-family: "Bebas Neue", sans-serif;
    text-shadow: 0px 100px 80px rgba(255, 107, 0, 0.11),
      0px 46.233px 36.9864px rgba(255, 107, 0, 0.0815843),
      0px 26.4535px 21.1628px rgba(255, 107, 0, 0.0689459),
      0px 16.0571px 12.8457px rgba(255, 107, 0, 0.0593943),
      0px 9.67509px 7.74008px rgba(255, 107, 0, 0.0506057),
      0px 5.38772px 4.31018px rgba(255, 107, 0, 0.0410541),
      0px 2.31722px 1.85378px rgba(255, 107, 0, 0.0284157);
    svg {
      position: absolute;
      width: 15rem;
      top: -1rem;
      right: -8rem;
    }
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
    svg {
      position: absolute;
      width: 15rem;
      top: 5rem;
      right: -5rem;
    }
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
    @media (max-width: 20em) {
      flex-direction: column;
      justify-content: center;
      align-items: center;
    }
    max-width: 130rem;
    display: flex;
    flex-wrap: wrap;
    position: relative;
    z-index: 10;
    justify-content: space-around;
    gap: 2rem;
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
      margin-left: 0;
      width: 100%;
      text-align: center;
      img {
        display: none;
      }
    }
    font-family: "Bebas Neue", sans-serif;
    font-size: 11rem;
    color: --main-font-color;
    width: 73.1rem;
    line-height: 11rem;
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
    @media (max-width: 48em) {
      margin-left: 0;
    }
    margin-top: 2rem;
    color: #444444;
    font-size: 2.4rem;
    margin-left: 12.8rem;
    line-height: 3.4rem;
    margin-bottom: 4rem;
  }
  &__btn {
    @media (max-width: 48em) {
      margin-left: 0;
    }
    color: white;
    background-color: #e2001a;
    border: none;
    border-radius: 1.5rem;
    padding: 1.8rem 3rem;
    font-size: 1.6rem;
    font-weight: 600;
    cursor: pointer;
    margin-left: 12.8rem;
    &:hover {
      background-color: #fc142f;
      transition: 0.2s;
    }
    &:active {
      box-shadow: inset 0px 3px 0px #d10018;
    }
  }
  &__text {
    position: relative;
    z-index: 10;
    margin-top: 29rem;
  }
  &__main {
    @media (max-width: 48em) {
      flex-direction: column-reverse;
      text-align: center;
      margin-bottom: 4rem;
    }
    display: flex;
  }
  &__container {
  }
  &__img {
    @media (max-width: 48em) {
      right: 0;
      max-height: 20rem;
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
    @media (max-width: 48em) {
      display: none;
    }
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
    @media (max-width: 48em) {
      right: 8rem;
    }
    position: relative;
    width: 5rem;
    height: 4.5rem;
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
    @media (max-width: 48em) {
      right: 0rem;
      bottom: 50rem;
    }
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
    @media (max-width: 48em) {
      bottom: 55rem;
      left: -15rem;
      width: 7rem;
      height: 7rem;
    }
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
    @media (max-width: 48em) {
      bottom: 75rem;
      right: 32rem;
      width: 7.5rem;
      height: 7.5rem;
    }
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
      isRequestSend: false,
    };
  },
};
</script>
