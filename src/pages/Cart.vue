<template>
  <div>
    <h1>Cart</h1>
    <div v-if="cart.length === 0">Your cart is empty.</div>
    <ul v-else>
      <li v-for="item in cart" :key="item.id">{{ item.name }} - ${{ item.price }}</li>
    </ul>
  </div>
</template>

<script>
import { ref } from 'vue';

export default {
  setup() {
    const cart = ref([]);
    return { cart };
  },
};
</script>

