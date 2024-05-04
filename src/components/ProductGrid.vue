<template>
  <div class="product-grid">
    <ProductCard 
      v-for="product in products" 
      :key="product.id" 
      :product="product" />
  </div>
</template>

<script>
import ProductCard from './ProductCard.vue';

export default {
  name: 'ProductGrid',
  components: {
    ProductCard
  },
  props: {
    products: Array
  }
}
</script>

<style scoped>
.product-grid {
  display: grid;
  grid-template-columns: repeat(3,1fr);
  grid-template-rows: auto auto;
  justify-content: space-around;
  gap: 20px;
}

@media (max-width: 768px) {
  .product-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 480px) {
  .product-grid {
    grid-template-columns: repeat(1, 1fr);
  }
}

</style>
