<template>
  <div>
    <header-component />
    <router-view></router-view>
  </div>
</template>

<script>
import HeaderComponent from '@/components/HeaderComponent.vue'
  export default {
  components: { HeaderComponent },
    
  }
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;700;800&family=Mulish:wght@900&display=swap');
*, *::after, *::before{
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
body  {
  max-width: 1440px;
  margin: 0 auto;
  font-family: 'Inter', sans-serif;
}
li  {
  list-style-type: none;
}
a {
  text-decoration: none;
}
.conteiner  {
  padding: 0 34px;
}
</style>