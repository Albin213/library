 <!-- <template>
    <div class="pa-6">
      <v-card v-if="book">
        <v-img :src="book.coverImage" :alt="bookTitle" height="400"></v-img>
  
        <v-card-title>{{ bookTitle }}</v-card-title>
        <v-card-subtitle>{{ book.author }}</v-card-subtitle>
  
        <v-card-text>
          <p>{{ book.description }}</p>
        </v-card-text>
      </v-card>
       <v-alert v-else-if="loading" type="info">Loading...</v-alert>
      <v-alert v-else type="error">Error loading book details.</v-alert> -->
    <!-- </div>
  </template>
  
  <script>
  import axios from 'axios';
  
  export default {
    async asyncData({ params }) {
      const bookId = params.id;
      try {
        const response = await axios.get(`http://192.168.1.65:5000/api/v1/amc/admin/all_books/${bookId}`);
        return {
          book: [response.data],
          loading: false,
        };
      } catch (error) {
        console.error('Error fetching book details:', error);
        return {
          book: null,
          loading: false,
        };
      }
    },
    data() {
      return {
        book: null,
        loading: true,
      };
    },
  };
  </script>
  


 -->



   <!-- <template>
    <div>
      <h1>Book List</h1>
      <button @click="fetchBooks">View Books</button>
  
      <ul v-if="books.length">
        <li v-for="book in books" :key="book.id">{{ book.title }}</li>
      </ul>
  
      <p v-else-if="loading">Loading...</p>
      <p v-else>Error loading book list.</p>
    </div>
  </template>
  
  <script>
  import axios from 'axios';
  
  export default {
    data() {
      return {
        books: [],
        loading: false,
      };
    },
    methods: {
      async fetchBooks() {
        this.loading = true;
        try {
          const response = await axios.get('http://192.168.1.51:5000/api/v1/amc/admin/all_books'); // Replace with your API endpoint
          this.books = response.data;
          this.loading = false;
        } catch (error) {
          console.error('Error fetching book list:', error);
          this.loading = false;
        }
      },
    },
  };
  </script> -->








  <template>
    <v-card>
        <v-img src="image1.jpg"></v-img>
    </v-card>
  </template>
   