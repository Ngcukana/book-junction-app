<template>
  <div class="container">
    <h1>Enter Book Details</h1>
    <form @submit.prevent="saveBook">
      <label for="bookId">Book ID (Generated)</label>
      <input type="text" id="bookId" v-model="bookDetails.bookId" readonly>

      <label for="isbn">ISBN</label>
      <input type="text" id="isbn" v-model="bookDetails.isbn" placeholder="Enter ISBN">

      <label for="author">Author</label>
      <input type="text" id="author" v-model="bookDetails.author" placeholder="Enter Author Name">

      <label for="title">Title</label>
      <input type="text" id="title" v-model="bookDetails.title" placeholder="Enter Book Title">

      <label for="edition">Edition</label>
      <input type="text" id="edition" v-model="bookDetails.edition" placeholder="Enter Edition">

      <label for="publisher">Publisher</label>
      <input type="text" id="publisher" v-model="bookDetails.publisher" placeholder="Enter Publisher">

      <label for="price">Price</label>
      <input type="number" id="price" v-model="bookDetails.price" placeholder="Enter Price">

      <button type="submit">Save Book Details</button>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      bookDetails: {
        bookId: '123456',
        isbn: '',
        author: '',
        title: '',
        edition: '',
        publisher: '',
        price: null
      }
    };
  },
  methods: {
    saveBook() {
      // Logic to save book details can be added here
      console.log('Book details saved:', this.bookDetails);
    }
  }
};
</script>

<style scoped>
body {
  font-family: Arial, sans-serif;
  background-color: #F0EFEB; /* Background color */
  color: #283618; /* Primary text color */
  margin: 0;
  padding: 0;
}
.container {
  max-width: 600px;
  margin: 50px auto;
  padding: 20px;
  background-color: #B7B7A4; /* Form background color */
  border-radius: 8px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}
h1 {
  text-align: center;
  color: #283618;
  margin-bottom: 20px;
}
label {
  display: block;
  margin-bottom: 8px;
  font-weight: bold;
  color: #283618;
}
input[type="text"],
input[type="number"] {
  width: 100%;
  padding: 10px;
  margin-bottom: 15px;
  border: 1px solid #D4D4D4;
  border-radius: 4px;
  background-color: #F0EFEB;
}
button {
  width: 100%;
  padding: 12px;
  background-color: #283618; /* Button background */
  color: #F0EFEB; /* Button text color */
  border: none;
  border-radius: 4px;
  cursor: pointer;
  font-size: 16px;
}
button:hover {
  background-color: #D4D4D4; /* Button hover color */
  color: #283618;
}
</style>
