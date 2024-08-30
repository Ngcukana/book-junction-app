<template>
  <div class="user-details">
    <h1>User Details</h1>
    <form @submit.prevent="handleSubmit">
      <label for="userid">User ID:</label>
      <input type="text" id="userid" v-model="formData.userid" required>

      <label for="name">Name:</label>
      <input type="text" id="name" v-model="formData.name" required>

      <label for="email">Email:</label>
      <input type="email" id="email" v-model="formData.email" required>

      <label for="cellphone">Cellphone Number:</label>
      <input type="tel" id="cellphone" v-model="formData.cellphone" required>

      <input type="submit" value="Submit">
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      formData: {
        userid: '',
        name: '',
        email: '',
        cellphone: ''
      }
    };
  },
  methods: {
    handleSubmit() {
      // Handle form submission
      console.log(this.formData);
      // Here, you can add your logic to process the form data.
    }
  }
};
</script>

<style scoped>
.user-details {
  background-color: #b7b7a4;
  font-family: Arial, sans-serif;
  color: #333;
  padding: 20px;
}

form {
  background-color: #fff;
  padding: 15px;
  border-radius: 5px;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
}

label {
  display: block;
  margin-top: 10px;
}

input[type="text"], input[type="email"], input[type="tel"] {
  width: 100%;
  padding: 8px;
  margin-top: 5px;
  border-radius: 3px;
  border: 1px solid #ccc;
}

input[type="submit"] {
  margin-top: 15px;
  padding: 10px 15px;
  background-color: #4CAF50;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

input[type="submit"]:hover {
  background-color: #45a049;
}
</style>