<!-- src/views/BookListing.vue -->
<template>
  <div>
    <h1>Book Listing</h1>
    <ul>
      <li v-for="book in books" :key="book.id">{{ book.title }} by {{ book.author }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'BookListing',
  data() {
    return {
      books: [
        { id: 1, title: 'Book One', author: 'Author A' },
        { id: 2, title: 'Book Two', author: 'Author B' },
        // Add more book data as needed
      ],
    };
  },
};
</script>

<style scoped>
/* Add styles for BookListing.vue */
</style>
