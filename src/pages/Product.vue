<template>
  <div>
    <h1>{{ product.name }}</h1>
    <p>{{ product.description }}</p>
    <p>Price: ${{ product.price }}</p>
    <button @click="addToCart(product)">Add to Cart</button>
  </div>
</template>

<script>
import { products } from '../mock/products.js';
import { useRoute } from 'vue-router';

export default {
  setup() {
    const route = useRoute();
    const product = products.find((p) => p.id === Number(route.params.id));
    const addToCart = (product) => {
      console.log('Added to cart:', product);
    };
    return { product, addToCart };
  },
};
</script>

