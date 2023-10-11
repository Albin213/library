<!-- <template>
    <v-form>
    <v-text-field
     label="searchbook"
     append-icon="mdi-window-close"
     v-model="bookname"
     ></v-text-field>

     



     <v-card color= "cyan darken-1" class="pa-6">
              <v-row >
                <v-col cols="12" sm="8">
                  <v-list-item three-line>
                    <v-list-item-content>
                      <div class="mb-4">
                        <v-btn fab color="cyan darken-1" elevation="0">
                          <v-icon color="white">fa-solid fa-book</v-icon>
                        </v-btn>
                      </div>
                      <v-list-item-title class="headline mb-1 white--text">
                        Library Book Management
                      </v-list-item-title>
                    </v-list-item-content>
                  </v-list-item>
                </v-col>
               
                    <v-col>
                       <div class="pt-13">
                  <v-btn
                  color="secondary" >Add A New Book</v-btn>
                       </div>
                </v-col>
              </v-row>
            </v-card>






     <script>
        export default{
            data(){
                return{
                    bookname:""
                }
            }
        }
     </script>

</v-form>
</template> -->








<!-- 

<template>
    <v-form>
      <v-text-field
        label="searchbook"
        append-icon="mdi-window-close"
        v-model="bookname"
      ></v-text-field>
  
      <v-card color="cyan darken-1" class="pa-6">
        <v-row>
          <v-col cols="12" sm="8">
            <v-list-item three-line>
              <v-list-item-content>
                <div class="mb-4">
                  <v-btn fab color="cyan darken-1" elevation="0">
                    <v-icon color="white">fa-solid fa-book</v-icon>
                  </v-btn>
                </div>
                <v-list-item-title class="headline mb-1 white--text">
                  Library Book Management
                </v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </v-col>
  
          <v-col>
            <div class="pt-13">
              <v-btn color="secondary" @click="navigateToAddBook">Add A New Book</v-btn>
            </div>
          </v-col>
        </v-row>
      </v-card>
    </v-form>
  </template>
  
  <script>
  export default {
    data() {
      return {
        bookname: ""
      };
    },
    methods: {
      navigateToAddBook() {
        // Use $router.push to navigate to the 'add-book' route
        this.$router.push({ name: "booklist" });
      }
    }
  };
  </script>
  
  <style scoped>
  /* Your component-specific styles go here */
  </style>
   -->


   <!-- <template>
    <div class="pa-6">
      <v-card color="cyan darken-1" class="pa-6">
        <v-col cols="12" sm="8">
          <v-list-item three-line>
            <v-list-item-content>
              <div class="mb-4">
                <v-btn fab color="cyan darken-1" elevation="0">
                  <v-icon
                    size="large"
                    color="green-darken-2"
                    icon="mdi-domain"
                  ></v-icon>
                   <v-icon color="black" icon="fa-book" size="large"></v-icon> -->
                <!-- </v-btn>
              </div>
              <v-list-item-title class="headline mb-1 white--text">
                Library Book Management
              </v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-col>
        <v-col>
          <div class="pt-13">
            <v-btn @click="addBookStatus" color="secondary">
              Add A New Book
            </v-btn>
            <v-btn @click="getBookList">Book List</v-btn>
          </div> -->
        <!-- </v-col>
        <div>
          <v-snackbar v-model="snackAlert">
            getBookList
            <template v-slot:action="{ attrs }">
              <v-btn color="pink" text v-bind="attrs" @click="snackAlert = false">
                Close
              </v-btn>
            </template>
          </v-snackbar>
          <v-form ref="form">
            <v-dialog v-model="dialog" persistent max-width="600px">
              <v-card>
                <v-card-title>
                  <span class="text-h5">Book Details</span>
                </v-card-title>
                <v-card>
                  <v-card-title>
                    {{ title }}
                  </v-card-title>
                  <v-card-text>{{ author }}</v-card-text>
                </v-card>
  
                <v-card-actions>
                  <v-spacer></v-spacer>
  
                  <v-btn color="blue" text> close </v-btn>
                </v-card-actions>
              </v-card>
            </v-dialog>
          </v-form>
        </div>
      </v-card>
    </div>
  </template> -->
  
  <!-- <script>
  import axios from "axios";
  export default {
    data() {
      return { -->
        <!-- //   navigateToAddBook,
        newbookname: "",
        bibloId: "",
        items: {},
        categorie: "",
        title: "",
        author: "",
        category: "",
        publisher: "",
        accessionno: "",
        imageFile: false,
        itemsList: [],
        newBookName: "",
        snackAlert: false,
        dialog: false,
        kjkrj: "",
      };
    },
    // mounted(){
    //   this.getBookList();
    // },
    methods: {
      addBookStatus() {
        this.$router.push({ name: "addbook" });
      },
    },
    async getBookList() {
    try {
      const response = await axios.get(`${process.env.apiUrl}admin/all_books`);
      const bookList = response.data; // Assuming the API returns an array of book objects
  
      // Assuming you want to update the component's data property named 'books'
      this.books = bookList;
    } catch (error) {
      console.error("Error fetching book list", error);
    }
  }
  
  };
  </script>
  <style>
  .mx-auto {
    color: #d9c8c8;
  }
  </style> -->











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
  <v-card>
    <v-card-title>{{ book.title }}</v-card-title>
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
          <v-form ref="form">
            <v-dialog v-model="dialog" persistent max-width="600px">
              <v-card>
                <v-card-title>
                  <span class="text-h5">Book Details</span>
                </v-card-title>
                <v-card>
                  <v-card-title>
                    {{ title }}
                  </v-card-title>
                  <v-card-text>{{ author }}</v-card-text>
                </v-card>
  
                <v-card-actions>
                  <v-spacer></v-spacer>
                  <v-btn color="blue" text @click="closeDialog">Close</v-btn>
                </v-card-actions>
              </v-card>
            </v-dialog>
          </v-form>
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
        booklist:[]
      };
    },
    methods: {
      addBookStatus() {
        this.$router.push({ name: "addbook" });
      },
      async fetchBookList() {
        try {
          const response = await axios.get(`${process.env.apiUrl}admin/all_books`);
          const books = response.data;
        
          // this.books = bookList; // Update the 'books' property with fetched data
          console.log(books);
          this.showSnackBar("Book list fetched successfully.");
        } catch (error) {
          console.error("Error fetching book list", error);
          this.showSnackBar("Error fetching book list.");
        }
      },







    //   methods: {
    //   fetchBookList() {
    // const apiUrl = 'http://192.168.1.73:5000/api/v1/amc/admin/all_books';

    // axios.get(apiUrl)
    //   .then(response => {
    //     // Handle the successful response here
    //     console.log(response.data); // This will log the API response data to the console
    //   })
    //   .catch(error => {
    //     // Handle any errors here
    //     console.error('Error:', error);
    //   });





      showSnackBar(message) {
        this.snackAlert = true;
        setTimeout(() => {
          this.snackAlert = false;
        }, 3000);
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
  