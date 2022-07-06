<template>
  <div id="app">
    <h1>Fabian Oberli Modul 291 </h1>
    <div id="nav">
      <router-link to="/home">Home</router-link> |
      <router-link to="/message">T-Shirt Shop</router-link> |
      <router-link to="/about">Discount Calculator</router-link> |
      <router-link to="/validation">Validation</router-link>
    </div>
    <router-view/>
  </div>
</template>

<script>
export default {
  components: {
  }
}
</script>

<style lang="scss">
@import 'styles/global';
</style>
