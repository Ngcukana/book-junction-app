<!-- src/components/SignIn.vue -->
<template>
  <div>
    <h1>Sign In</h1>
    <form @submit.prevent="signIn">
      <label for="email">Email:</label>
      <input type="email" v-model="email" id="email" required />

      <label for="password">Password:</label>
      <input type="password" v-model="password" id="password" required />

      <button type="submit">Sign In</button>
    </form>
  </div>
</template>

<script>
export default {
  name: 'SignIn',
  data() {
    return {
      email: '',
      password: '',
    };
  },
  methods: {
    signIn() {
      // Handle sign in logic here
      console.log(`Signing in with ${this.email} and ${this.password}`);
    },
  },
};
</script>

<style scoped>
/* Add styles for SignIn.vue */
</style>
