<template>
  <div id="app">
    <ProductList />
  </div>

  <!-- CAMBIO DE TEST PARA CLAVE SSH -->

</template>

<script>
import ProductList from './components/ProductList.vue';

export default {
  name: 'App',
  components: {
    ProductList
  }
}
</script>

<style>

html, body {
  background-color: #EAEDED;
  font-family: 'Exo 2', sans-serif;
}

.app {
  height: 100%;
}
</style>
