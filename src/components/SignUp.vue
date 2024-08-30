<!-- src/components/SignUp.vue -->
<template>
  <div>
    <h1>Sign Up</h1>
    <form @submit.prevent="signUp">
      <label for="email">Email:</label>
      <input type="email" v-model="email" id="email" required />

      <label for="password">Password:</label>
      <input type="password" v-model="password" id="password" required />

      <label for="confirmPassword">Confirm Password:</label>
      <input type="password" v-model="confirmPassword" id="confirmPassword" required />

      <button type="submit">Sign Up</button>
    </form>
  </div>
</template>

<script>
export default {
  name: 'SignUp',
  data() {
    return {
      email: '',
      password: '',
      confirmPassword: '',
    };
  },
  methods: {
    signUp() {
      if (this.password !== this.confirmPassword) {
        alert("Passwords do not match");
        return;
      }
      // Handle sign up logic here
      console.log(`Signing up with ${this.email}`);
    },
  },
};
</script>

<style scoped>
/* Add styles for SignUp.vue */
</style>
