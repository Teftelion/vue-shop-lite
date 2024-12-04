<template>
  <div class="product-list">
    <ProductCard
      v-for="product in products"
      :key="product.id"
      :product="product"
      @add-to-cart="addToCart"
    />
  </div>
</template>

<script>
import ProductCard from './ProductCard.vue';
import { products } from '../mock/products.js';

export default {
  components: { ProductCard },
  setup() {
    const cart = [];
    const addToCart = (product) => {
      cart.push(product);
      console.log('Cart:', cart);
    };
    return { products, addToCart };
  },
};
</script>

