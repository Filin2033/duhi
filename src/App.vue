<template>
  <div id="app">
    <div class="product-list d-flex"> 
      <ProductCard 
        v-for="product in products"
        :key="product.id" 
        :product="product"
      />
    </div>
  </div>
</template>

<script>
import ProductCard from './components/ProductCard.vue';

export default {
  components: {
    ProductCard
  },
  data() {
    return {
      products: [
        {
          id: 1,
          imageUrl: '123.png', 
          category: 'ПАРФЮМЕРНЫЙ ЭКСТРАКТ',
          name: 'FRAGRANCE DU BOIS HERITAGE',
          oldPrice: '2500₽',
          price: '1990₽'
        }
      ]
    };
  }
};
</script>

<style>
@import './global.css'; 

.product-list {
  flex-wrap: wrap;
  justify-content: space-around;
}
</style>