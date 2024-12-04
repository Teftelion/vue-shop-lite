<template>
  <div class="product-card">
    <h3>{{ product.name }}</h3>
    <p>Price: ${{ product.price }}</p>
    <button @click="$emit('add-to-cart', product)">Add to Cart</button>
    <router-link :to="`/product/${product.id}`">View Details</router-link>
  </div>
</template>

<script>
export default {
  props: ['product'],
};
</script>

