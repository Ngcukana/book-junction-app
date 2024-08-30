<!-- src/App.vue -->
<template>
  <div id="app">
    <nav>
      <router-link to="/">Home</router-link>
      <router-link to="/signin">Sign In</router-link>
      <router-link to="/signup">Sign Up</router-link>
      <router-link to="/SellABook">Sell Book</router-link>
      <router-link to="/SellerDetails">Seller Details</router-link>
    </nav>
    <router-view></router-view>
  </div>
</template>

<script>
export default {
  name: 'App',
};
</script>

<style>
/* Add global styles here */
nav {
  margin-bottom: 20px;
}
nav a {
  margin: 0 10px;
}
</style>

