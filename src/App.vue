<script setup>
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <div class="min-h-screen bg-gray-100">
    <NavBar :cartItemCount="cartItems.length" />
    <router-view 
      :courses="courses" 
      :cartItems="cartItems" 
      @add-to-cart="addToCart" 
      @remove-from-cart="removeFromCart"
      @remove-selected="removeSelected"
      @checkout="checkout"
    />
  </div>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
