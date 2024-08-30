<template>
  <div id="app">
    <header>
      <h1>Book Junction</h1>
    </header>
    <main>
      <h2>Sell A Book</h2>
      <button @click="login">Login</button>
      <button @click="createProfile">Create a Profile</button>
    </main>
  </div>
</template>

<script>
export default {
  name: 'BookJunction',
  methods: {
    login() {
      alert('Login button clicked!');
    },
    createProfile() {
      alert('Create a Profile button clicked!');
    }
  }
}
</script>

<style>
body {
  background-color: #B7B7A4; /* Light gray-green color */
  font-family: Arial, sans-serif;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100vh;
  margin: 0;
}
header {
  background-color: #283618; /* Dark green-gray color */
  color: white;
  text-align: center;
  padding: 20px;
  width: 100%;
  position: absolute;
  top: 0;
}
h1 {
  font-size: 2.5em; /* Large font size for title */
  margin: 0;
}
h2 {
  font-size: 4.5em; /* Large font size for heading */
  margin: 0;
}
button {
  background-color: #283618; /* Dark green-gray color for buttons */
  color: white;
  border: none;
  border-radius: 5px;
  padding: 10px 20px;
  font-size: 1.2em; /* Button font size */
  margin: 10px;
  cursor: pointer;
  transition: background-color 0.3s;
}
button:hover {
  background-color: #1c2d27; /* Darker shade on hover */
}
</style>