<template>
  <main class="home conteiner">
    <div class="home__inner">
      <h1 class="home__title">оборудование для майнинга</h1>
      <p class="home__subtitle">По оптовым ценнам</p>
      <div class="home__btn-wrapper">
        <my-button class="home__btn">получить актуальные ценны</my-button>
      </div>
      <div class="home__img-wrapper">
        <img src="@/assets/illustration/mining.png" alt="" class="home__img">
      </div>
    </div>
  </main>
</template>

<script>
import MyButton from '@/components/UI/MyButton.vue'
  export default {
  components: {
  MyButton
}
    
  }
</script>

<style lang="scss" scoped>
  .home {
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
</style>