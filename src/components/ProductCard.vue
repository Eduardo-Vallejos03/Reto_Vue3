<template>
  <div class="product-card">
    <img :src="getImageUrl(product.image)" :alt="product.name" class="product-image">
    <h3>{{ product.name }}</h3>
    <p>${{ product.price }}</p>
    <ProductButtons/>
  </div>
</template>

<script>
import ProductButtons from './ProductButtons.vue';

export default {
  name: 'ProductCard',
  components: {
    ProductButtons
  },
  props: {
    product: {
      type: Object,
      required: true
    }
  },
  methods: {
    getImageUrl(imageName) {
      return require(`@/assets/img/${imageName}`);
    }
  }
}
</script>

<style scoped>
.product-card {
  background-color: white;
  border: 1px solid #D7DBDD;
  border-radius: 8px;
  padding: 10px;
  text-align: center;
  box-shadow: 0 2px 6px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.product-card:hover {
  transform: translateY(-1px);
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
}

.product-image {
  width: 100%;
  max-width: 200px;
  height: 200px;
  display: block;
  margin: 0 auto;
}
</style>
