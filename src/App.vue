<template>
  <div id="app">
    <div class="nav-bar"></div>
    <div class="cart">Cart({{ cart }})</div>
    <ProductDisplay :premium="premium" @add-to-cart="updateCart"></ProductDisplay>
  </div>
</template>

<script>
import ProductDisplay from "./components/ProductDisplay";

export default {
  name: 'App',
  data() {
    return {
      cart: 0,
      premium: true
    }
  },
  computed: {
    ProductDisplay
  },
  methods: {
    updateCart() {
      this.cart += 1
    }
  },
  components: {
    ProductDisplay

  }
}
</script>

<style>
@import './assets/styles.css';
</style>
