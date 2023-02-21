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
*, *::after, *::before{
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
body  {
  max-width: 1440px;
  margin: 0 auto;
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