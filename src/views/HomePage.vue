<template>
  <div class="home-page">
    <main class="home-bg conteiner">
      <div class="home-bg__inner">
        <h1 class="home-bg__title">оборудование для майнинга</h1>
        <p class="home-bg__subtitle">По оптовым ценнам</p>
        <div class="home-bg__btn-wrapper">
          <my-button class="home-bg__btn">получить актуальные ценны</my-button>
        </div>
        <div class="home-bg__img-wrapper">
          <img src="@/assets/illustration/mining.png" alt="" class="home__img">
        </div>
      </div>
    </main>
    <section class="home-info conteiner">
      <div class="home-info__inner">
        <div class="home-info__title-wrapper">
          <h2 class="home-info__title">предлагаем готовые решения</h2>
        </div>
        <div class="home-info__items">
          <div class="home-info__item" v-for="item in infoState" :key="item.img">
            <div class="home-info__item-title-wrapper">
              <div class="home-info__item-img-wrapper">
                <img :src="require(`@/assets/svg/${item.img}.svg`)" :alt="item.img">
              </div>
              <h4 class="home-info__item-title">{{ item.title }}</h4>
            </div>
            <p class="home-info__item-subtitle">{{ item.subtitle }}</p>
          </div>
        </div>
        <div class="home-info__btn-wrapper">
          <my-button class="home-info__btn">хочу знать больше</my-button>
        </div>
      </div>
    </section>
    <section class="home-hit conteiner">
      <div class="home-hit__inner">
        <div class="home-hit__title-wrapper">
          <h2 class="home-hit__title">хиты продаж</h2>
          <div class="home-hit__title-img">
            <img src="@/assets/svg/fire.svg" alt="fire">
          </div>
        </div>
        <p class="home-hit__subtitle">Цена указана в розницу. Больше устройств - больше скидка</p>
        <div class="home-hit__products">
          <div class="home-hit__product" v-for="product in products" :key="product.nameProduct">
            <div class="home-hit__product-img-wrapper">
              <img class="home-hit__product-img" :src="require(`@/assets/productsImg/${product.img}.png`)" alt="">
            </div>
            <h5 class="home-hit__product-subtitle">{{ product.categorie }}</h5>
            <h4 class="home-hit__product-name">{{ product.nameProduct }}</h4>
            <div class="home-hit__product-price-wrapper">
              <h4 class="home-hit__product-price">{{ product.price }} ₽</h4>
              <img src="@/assets/svg/firePrice.svg" alt="" class="home-hit__price-fire">
            </div>
          </div>
        </div>
        <div class="home-hit__products-btn-wrapper">
           <my-button class="home-hit__products-btn">перейти в каталог</my-button>
        </div>
       
      </div>
    </section>
    <section class="home-connect conteiner">
      <div class="home-connect__inner">
        <div class="home-connect__title-wrapper">
          <h2 class="home-connect__title">подключение к пулу на выгодных условиях</h2>
          <my-button class="home-connect__btn">подключиться к пулу</my-button>
        </div>
        <div class="home-connect__list">
          <div class="home-connect__list-items">
            <div class="home-connect__list-item" v-for="item in connectItems" :key="item.title">
              <img :src="require(`@/assets/svg/${item.img}.svg`)" alt="" class="home-connect__item-img">
              <h4 class="home-connect__item-title">{{ item.title }}</h4>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="home-partners conteiner">
      <div class="home-partners__inner">
        <h2 class="home-partners__title">Мы являемся эксклюзивным партнером</h2>
        <img src="@/assets/svg/btcLogo.svg" alt="btcLogo">
      </div>
    </section>
    <section class="home-machine-mg conteiner">
      <div class="home-machine-mg__inner">
        <h2 class="home-machine-mg__title">подбери свое оборудование для майнинга</h2>
        <div class="home-machine-mg__items">
          <div class="home-machine-mg__item" v-for="item in machineItems" :key="item.img">
            <div class="home-machine-mg__img-wrapper">
              <img :src="require(`@/assets/svg/${item.img}.svg`)" :alt="item.img" class="home-machine-mg__item-img">
            </div>
            <h4 class="home-machine-mg__item-title">{{ item.title }}</h4>
            <p class="home-machine-mg__item-subtitle">{{ item.subtitle }}</p>
          </div>
        </div>
        <div class="home-machine-mg__btn-wrapper">
          <my-button>заказать звонок</my-button>
        </div>
      </div>
    </section>
    <section class="home-choice">
      <div class="homne-choice__inner">
        <div class="home-choice__images-wrapper">
          <img src="@/assets/productsImg/pr6.png" alt="" class="home-choice__img">
          <img src="@/assets/productsImg/pr7.png" alt="" class="home-choice__img">
        </div>
        <div class="home-choice__content">
          <h2 class="home-choice__title">Подберем нужный ASIC</h2>
          <h4 class="home-choice__subtitle">Закажите консультацию и мы поможем вам в подборе оборудования</h4>
          <my-button>заказать консультацию</my-button>
        </div>
      </div>
    </section>
  </div>
  
</template>

<script>
import MyButton from '@/components/UI/MyButton.vue'
  export default {
  components: {
  MyButton
},
    data ()
  {
      return {
        infoState: [
          { img: 'fork', title: 'Продажа оборудования', subtitle: 'Доставка в любую точку мира Оптовые цены на оборудование Гарантия на все наши товары' },
          { img: 'like', title: 'Размещение на хостинге', subtitle: 'Дата-центры от 3.5 рублей за кВт*ч Майнинг отели по всей России Бесплатная установка оборудования' },
          { img: 'chain', title: 'Подключение к пулу', subtitle: 'Официальные представители ViaBTC Выгодные условия сотрудничества Техподдержка онлайн 24/7' },
        ],
        products: [
          { img: 'pr1', categorie: 'BITMAIN, ASIC-МАЙНЕРЫ, АСИКИ S19', nameProduct: 'Antminer S19 90Th', price: '200500' },
          { img: 'pr2', categorie: 'BITMAIN, ASIC-МАЙНЕРЫ, АСИКИ S19', nameProduct: 'WhatsMiner M30S++', price: '200500' },
          { img: 'pr3', categorie: 'BITMAIN, ASIC-МАЙНЕРЫ, АСИКИ S19', nameProduct: 'WhatsMiner M32S', price: '192500' },
          { img: 'pr4', categorie: 'BITMAIN, ASIC-МАЙНЕРЫ, АСИКИ S19', nameProduct: 'Antminer S19 90Th', price: '200500' },
          { img: 'pr5', categorie: 'BITMAIN, ASIC-МАЙНЕРЫ, АСИКИ S19', nameProduct: 'WhatsMiner M30S++', price: '200500' },
        ],
        connectItems: [
          { img: 'hightUptime', title: 'Высокий аптайм' },
          { img: 'shield', title: 'надежность' },
          { img: 'support', title: 'техподдержка 24/7' },
          { img: 'money', title: 'автовывод без комиссии' },
        ],
        machineItems: [
          { img: 'car', title: 'Удобная доставка', subtitle: 'По всей России и СНГ' },
          { img: 'dolars', title: 'Оптовые цены', subtitle: 'Работаем с крупными поставщиками' },
          { img: 'rocket', title: 'Быстрая консультация', subtitle: 'Находимся онлайн 24/7' },
          { img: 'save', title: 'Гарантия на оборудование', subtitle: 'Действует на все наше оборудование' },
        ]
      }
    }
  }
</script>

<style lang="scss" scoped>
  .home-bg {
    margin-bottom: 80px;
    &__inner  {
      position: relative;
      background: #232323;
      border-radius: 10px;
      display: flex;
      flex-direction: column;
    }
    &__title {
      padding: 73px 0 16px 82px;
      font-weight: 900;
      font-size: 44px;
      line-height: 48px;
      text-transform: uppercase;
      color: #ffffff;
      max-width: 600px;
      width: 100%;
    }
    &__subtitle {
      font-weight: 400;
      font-size: 24px;
      line-height: 29px;
      color: #ffffff;
      padding: 0px 0px 49px 82px;
    }
    &__btn-wrapper  {
      padding: 0px 0px 93px 82px;
    }
    &__btn  {
      background: linear-gradient(270deg, #7250E6 0%, #FF5C87 100%);
      border-radius: 10px;
      padding: 20px 39px;
      color: #ffffff;
    }
    &__img-wrapper  {
      position: absolute;
      right: 144px;
      top: -4px;
    }
  }
  .home-info  {
    &__inner  {
      display: flex;
      flex-direction: column;
    }
    &__title-wrapper  {
      margin-bottom: 36px;
    }
    &__title  {
      font-family: 'Mulish', sans-serif;
      font-weight: 900;
      font-size: 38px;
      line-height: 41px;
      text-transform: uppercase;
      color: #232323;
    }
    &__items  {
      display: flex;
      margin-bottom: 24px;
    }
    &__item {
      display: flex;
      flex-direction: column;
      width: 416px;
    }
    &__item-title-wrapper {
      display: flex;
      margin-bottom: 24px;
    }
    &__item-img-wrapper {
      width: 56px;
      height: 56px;
      background: #F5F5F5;
      border-radius: 10px;
      display: flex;
      justify-content: center;
      align-items: center;
      margin-right: 24px;
    }
    &__item-title {
      width: 288px;
      font-weight: 800;
      font-size: 24px;
      line-height: 29px;
      color: #232323;
    }
    &__item-subtitle  {
      font-weight: 400;
      font-size: 16px;
      line-height: 19px;
      color: #707070;
      width: 300px;
    }
    &__btn-wrapper  {
      display: flex;
      justify-content: center;
    }
    &__btn {
      background: #7250E6;
      border-radius: 10px;
      padding: 20px 48px;
      font-weight: 700;
      font-size: 14px;
      line-height: 15px;
      text-transform: uppercase;
      color: #FFFFFF;
    }
  }
  .home-hit {
    margin-bottom: 48px;
    &__title-wrapper  {
      display: flex;
      margin-bottom: 20px;
    }
    &__title  {
      font-weight: 900;
      font-size: 38px;
      line-height: 41px;
      text-transform: uppercase;
      color: #232323;
      font-family: 'Mulish', sans-serif;
    }
    &__title-img  {
      margin-left: 28px;
      height: 56px;
      width: 56px;
      background: #F5F5F5;
      border-radius: 10px;
      display: flex;
      justify-content: center;
      align-items: center;
    }
    &__subtitle {
      font-weight: 400;
      font-size: 16px;
      line-height: 19px;
      color: #414141;
      margin-bottom: 20px;
    }
    &__products {
      display: flex;
    }
    &__product  {
      background: #FFFFFF;
      border: 2px solid #D9D9D9;
      border-radius: 10px;
      display: flex;
      flex-direction: column;
      justify-content: flex-end;
      margin-right: 13px;
      align-items: center;
      height: 333px;
      width: 264px;
    }
    &__product:last-child {
      margin-right: 0;
    }
    &__product-subtitle {
      font-weight: 400;
      font-size: 10px;
      line-height: 12px;
      text-transform: uppercase;
      color: #B7B7B7;
    }
    &__product-name {
      font-family: 'Mulish', sans-serif;
      font-weight: 600;
      font-size: 21px;
      line-height: 30px;
      text-transform: uppercase;
      color: #000000;
    }
    &__product-price-wrapper  {
      display: flex;
      align-items: center;
      margin-bottom: 10px;
    }
    &__product-price  {
      font-family: 'Mulish', sans-serif;
      font-weight: 800;
      font-size: 28px;
      line-height: 30px;
      color: #232323;
      margin-right: 4px;
    }
    &__products-btn {
      background: #7250E6;
      border-radius: 10px;
      padding: 20px 48px;
      margin-top: 36px;
      color: #FFFFFF;
      font-weight: 700;
      font-size: 14px;
      line-height: 15px;
      text-transform: uppercase;
    }
    &__products-btn-wrapper {
      display: flex;
      justify-content: center;
    }
  }
  .home-connect {
    margin-bottom: 99px;
    &__inner  {
      background: #232323;
      border-radius: 10px;
      padding: 46px 0 59px 81px;
    }
    &__title-wrapper  {
      display: flex;
      align-items: center;
      margin-bottom: 61px;
    }
    &__title  {
      font-weight: 900;
      font-size: 38px;
      line-height: 41px;
      text-transform: uppercase;
      color: #FFFFFF;
      width: 842px;
    }
    &__btn  {
      background: linear-gradient(270deg, #7250E6 0%, #FF5C87 100%);
      border-radius: 10px;
      padding: 20px 47px;
      font-weight: 700;
      font-size: 14px;
      line-height: 15px;
      text-transform: uppercase;
      color: #FFFFFF;
    }
    &__list-items {
      margin-left: 2px;
      display: flex;
      align-items: center;
    }
    &__list-item  {
      margin-right: 37px;
      display: flex;
      align-items: center;
    }
    &__list-item:last-child {
      margin-right: 0;
    }
    &__item-img {
      margin-right: 25px;
    }
    &__item-title {
      font-weight: 600;
      font-size: 21px;
      line-height: 34px;
      text-transform: uppercase;
      color: #FFFFFF;
    }
  }
  .home-partners  {
    background: #F5F5F5;
    padding: 53px 0;
    margin-bottom: 80px;
    &__inner  {
      display: flex;
      justify-content: center;
      align-items: center;
    }
    &__title  {
      margin-right: 20px;
    }
  }
  .home-machine-mg  {
    &__inner  {
      margin-bottom: 80px;
      display: flex;
      flex-direction: column;
    }
    &__title  {
      font-family: 'Mulish', sans-serif;
      width: 725px;
      font-weight: 900;
      font-size: 38px;
      line-height: 41px;
      text-transform: uppercase;
      color: #232323;
      margin-bottom: 28px;
    }
    &__items  {
      display: flex;
      justify-content: space-between;
      margin-bottom: 36px;
    }
    &__item {
      display: flex;
      flex-direction: column;
    }
    &__img-wrapper  {
      width: 70px;
      height: 70px;
      border-radius: 10px;
      background: #F5F5F5;
      display: flex;
      justify-content: center;
      align-items: center;
      margin-bottom: 24px;
    }
    &__item-title {
      font-weight: 800;
      font-size: 24px;
      line-height: 29px;
      color: #232323;
      margin-bottom: 24px;
    }
    &__item-subtitle  {
      font-weight: 400;
      font-size: 16px;
      line-height: 19px;
      color: #707070;
    }
    &__btn-wrapper  {
      display: flex;
      justify-content: center;
    }
    &__inner > &__btn-wrapper > button{
      background: #7250E6;
      border-radius: 10px;
      padding: 20px 48px;
      font-weight: 700;
      font-size: 14px;
      line-height: 15px;
      text-transform: uppercase;
      color: #FFFFFF;
    }
  }
  .home-choice  {
    background: #232323;
    position: relative;
  }
</style>