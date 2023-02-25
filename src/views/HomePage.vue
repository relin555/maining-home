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
</style>