<template>
    <div class="pa-2">
      <v-card color="cyan darken-1" class="pa-6">
        <v-col cols="2" sm="6">
          <v-list-item three-line>
            <v-list-item-content>
              <div class="mb-18">
                <v-btn fab color="cyan darken-1" elevation="0">
                  <v-icon size="large" color="green darken-2" icon="mdi-domain"></v-icon>
                </v-btn>
              </div>
              <v-list-item-title class="headline mb-1 white--text">
                Library Book Management
              </v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-col>
        <v-col>
          <div class="pt-2">
            <v-btn @click="addBookStatus" color="secondary">
              Add A New Book
            </v-btn>
            <v-btn @click="fetchBookList">Book List</v-btn>
          </div>
        </v-col>
        <div>
            <v-col
            v-for="book in books"
            :key="book.id"
            cols="12"
            sm="6"
            md="4"
            lg="3"
          >
            <v-card @click="showBookDetails(book)">
              <v-card-title>{{ book.bookTitle}}</v-card-title>
              <v-card-text>
                <p>Author: {{ book.author }}</p>
                <p>Category: {{ book.category }}</p>
                <!-- Add more book details as needed -->
              </v-card-text>
            </v-card>
          </v-col>
          <v-snackbar v-model="snackAlert">
            <!-- Snackbar message -->
            Book list fetched successfully.
            <template v-slot:action="{ attrs }">
              <v-btn color="pink" text v-bind="attrs" @click="snackAlert = false">
                Close
              </v-btn>
            </template>
          </v-snackbar>
         
          <v-dialog v-model="dialog" persistent max-width="600px">
            <v-card>
              <v-card-title>
                <span class="text-h5">Book Details</span>
              </v-card-title>
              <v-card>
                <v-card-title>{{ selectedBook.bookTitle }}</v-card-title>
                <v-card-text>
                  <p>Author: {{ selectedBook.author }}</p>
                  <p>Category: {{ selectedBook.category }}</p>
                  <!-- Add more book details as needed -->
                </v-card-text>
              </v-card>
              <v-card-actions>
                <v-spacer></v-spacer>
                <v-btn color="blue" text @click="closeDialog">Close</v-btn>
              </v-card-actions>
            </v-card>
          </v-dialog>
        </div>
      </v-card>
    </div>
    
  </template>
  
  <script>
  import axios from "axios";
  
  export default {
    data() {
      return {
        newbookname: "",
        bibloId: "",
        categorie: "",
        title: "",
        author: "",
        category: "",
        publisher: "",
        accessionno: "",
        imageFile: false,
        books: [], // Initialize as an empty array to store the fetched books
        snackAlert: false,
        dialog: false,
        selectedBook: {}, // Store the selected book details
      };
    },
    methods: {
      addBookStatus() {
        this.$router.push({ name: "addbook" });
      },
      async fetchBookList() {
        try {
          const response = await axios.get(`${process.env.apiUrl}admin/all_books`);
          const booklist = response.data;
  
          this.books = booklist.docs; // Update the 'books' property with fetched data
          console.log(booklist);
          this.showSnackBar("Book list fetched successfully.");
        } catch (error) {
          console.error("Error fetching book list", error);
          this.showSnackBar("Error fetching book list.");
        }
      },
      showSnackBar(message) {
        this.snackAlert = true;
        setTimeout(() => {
          this.snackAlert = false;
        }, 3000);
      },
      showBookDetails(book) {
        this.selectedBook = book;
        this.dialog = true;
      },
      closeDialog() {
        this.dialog = false;
      },
    },
  };
  </script>
  
  <style>
  .mx-auto {
    color: #d9c8c8;
  }
  </style>
  
