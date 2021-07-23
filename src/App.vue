<template>
  <div id="app">
    <div class="nav-bar"></div>
    <div class="cart">Cart({{ cart.length }})</div>
    <product-display :premium="premium" @add-to-cart="updateCart" @remove-from-cart="removeFromCart"></product-display>
  </div>
</template>

<script>
import ProductDisplay from "./components/ProductDisplay";

export default {
  name: 'App',
  data() {
    return {
      cart: [],
      premium: true
    }
  },
  computed: {
    ProductDisplay
  },
  methods: {
    updateCart(id) {
      this.cart.push(id)
    },
    removeFromCart(id) {
      var index =  this.cart.indexOf(id);
      if (index > -1) {
        this.cart.splice(index, 1);
      }
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
