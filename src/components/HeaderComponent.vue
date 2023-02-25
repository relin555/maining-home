<template>
  <header class="header conteiner">
    <div class="header__inner">
      <div class="header__logo">
        <img src="@/assets/svg/logo.svg" alt="" class="logo">
      </div>
      <div class="header__search">
        <my-input v-model="searchInput" placeholder="Поиск" style=""/>
        <my-button>
          <img src="@/assets/svg/search.svg" alt="">
        </my-button>
      </div>
      <nav class="header__navigation">
        <ul class="header__nav-items">
          <li class="header__nav-item" v-for="item in linkRouter" :key="item.link">
            <router-link :to="item.path">{{ item.name }}</router-link>
          </li>
        </ul>
      </nav>
      <div class="header__contacts">
        <div class="header__contact-telegram">
          <my-button style="border:none;background:inherit;margin-right: 8px;">
            <img src="@/assets/svg/telegram.svg" alt="">
          </my-button>
        </div>
        <div class="header__contact-whattsapp">
          <my-button style="border:none;background:inherit;margin-right: 16px;">
            <img src="@/assets/svg/whatsapp.svg" alt="">
          </my-button>
        </div>
        <div class="header__phone">
          <a href="tel:+79810381762" class="header__phone-call">+7 981 03-81-762</a>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
import MyInput from '@/components/UI/MyInput.vue'
import MyButton from './UI/MyButton.vue'
  export default {
  components: {
    MyInput,
    MyButton  
  },
  data ()
  {
    return {
      searchInput: '',
      linkRouter: [
        { path: '/', name: 'Каталог' },
        { path: '/services', name: 'Услуги' },
        { path: '/deliveryandpaymant', name: 'Доставка и оплата' },
        { path: '/contacts', name: 'Контакты' },
        { path: '/about', name: 'О нас' },
        ]
      }
    }
  }
</script>

<style lang="scss" scoped>
  .header {
    &__inner  {
      display: flex;
      align-items: center;
      padding: 20px 0 20px 0;
    }
    &__logo {
      margin-right: 42px;
    }
    &__search {
      position: relative;
      margin-right: 42px;

    }
    &__search > input{
    width: 272px;
    height: 44px;
    background: #ECECEC;
    border-radius: 5px;
    border: none;
    outline: none;
    padding-left: 20px;
    padding-right: 90px;
    font-weight: 500;
    font-size: 16px;
    line-height: 19px;
    color: #707070;
    font-family: 'Inter';
    }
    &__search > input::placeholder{
      font-weight: 500;
      font-size: 16px;
      line-height: 19px;
      color: #707070;
      margin-left: 20px;
      font-family: 'Inter';
    }
    &__search > button  {
      position: absolute;
      display: flex;
      justify-content: center;
      align-items: center;
      padding: 7px 25px;
      background: #7250E6;
      border-radius: 5px;
      border: none;
      outline: none;
      left: 196px;
      top: 5px;
    }
    &__nav-items  {
      display: flex;
      align-items: center;
    }
    &__nav-item {
      margin-right: 40px;
    }
    &__nav-item:last-child  {
      margin-right: 42px;
    } 
    &__contacts  {
      display: flex;
      align-items: center;
    }
    &__phone > a {
      font-weight: 700;
      font-size: 16px;
      line-height: 19px;
      color: #232323;
    }
    
  }
  
  ul > li > a {
    color: #232323;
    font-weight: 500;
    font-size: 13px;
    line-height: 16px;
    text-transform: uppercase;
  }

</style>