<template>  
  
  <header>
    <div class="header">
        <h1>Listado</h1>
        <nav>
            <a href="#">Home</a>
            <a href="#">Productos</a>
        </nav>
    </div>
  </header>

  <main class="main">
    <div class="category-elements">
      <h2>Categorías</h2>
        <nav class="navegacion-aside">
          <a href="#" @click="filterByCategory('Todos', $event)"
          :class="{ active: activeCategory === 'Todos' }">Todos</a>
          <a href="#" @click="filterByCategory('mesa', $event)"
          :class="{ active: activeCategory === 'mesa' }">Mesas</a>
          <a href="#" @click="filterByCategory('lampara', $event)"
          :class="{ active: activeCategory === 'lampara' }">Lámparas</a>
          <a href="#" @click="filterByCategory('silla', $event)"
          :class="{ active: activeCategory === 'silla' }">Sillas</a>
          <a href="#" @click="filterByCategory('sofa', $event)"
          :class="{ active: activeCategory === 'sofa' }">Sofás</a>
        </nav>
    </div> 
    
    <div>
      <ProductGrid :products="productFilter" /> <!-- Pasamos el prop a Grid -->
    </div>
  </main>

</template> 

<script>
import ProductGrid from './ProductGrid.vue';
import productData from '@/assets/products.json';

export default {
  name: 'ProductList',
  components: {
    ProductGrid
  },
  data() {
    return {
      products: productData,
      productFilter: productData
    };
  },

methods: {
  filterByCategory(category, event) {
      event.preventDefault();
      this.activeCategory = category;
      this.productFilter = category === 'Todos' 
        ? this.products 
        : this.products.filter(product => product.category === category);
  }
}
}

</script>

<style>

/* HEADER */
.header {
    display: flex;
    flex-direction: column; 
    justify-content: center; 
    align-items: center; 
    text-align: center;
    margin-bottom: 3rem;
}

nav a {
    margin: 0 0.5rem;
    text-decoration: none;
    color: black;
}

h1 {
    margin-bottom: 2rem;
}

/* CATEGORY */
.category-elements{
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-around;
    background-color: #34495E;
    padding: 15px 50px;
    box-shadow: 10px 10px 20px rgba(0, 0, 0, 0.5);
    margin: 0 0 40px 0;
    color: white;
}


.navegacion-aside a {
    color: white;
    margin: 20px;
}


.navegacion-aside a.active { 
  border-bottom: 2px solid #fff; 
  
 }


/* CATEGORY RESPONSIVE */
@media (max-width: 768px) {
  .category-elements{
    display: flex;
    flex-direction: column;;
    align-items: center;
    justify-content: center;
  }
}

@media (max-width: 480px) {
  .navegacion-aside {
    display: flex;
    flex-direction: column;;
    align-items: center;
    justify-content: center;
  }
}
</style>