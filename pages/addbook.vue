<template>
    <div>
      <v-card>
        <v-card-title>
          <span class="text-h5">Book Details</span>
        </v-card-title>
        <v-card-text>
          <v-avatar size="62"> </v-avatar>
  
          <div>
            <form>
              <v-row>
                <v-col cols="12">
                  <v-text-field
                    label="Title"
                    v-model="title"
                    required
                  ></v-text-field>
                </v-col>
  
                <v-col cols="12" sm="6">
                  <v-text-field
                    label="Author"
                    v-model="author"
                    required
                  ></v-text-field>
                </v-col>
  
                <v-col cols="12" sm="6">
                  <v-text-field
                    label="Category"
                    v-model="category"
                    required
                  ></v-text-field>
                </v-col>
  
                <v-col cols="12" sm="6">
                  <v-text-field
                    label="Publisher"
                    v-model="publisher"
                    required
                  ></v-text-field>
                </v-col>
  
                <v-col cols="12" sm="6">
                  <v-text-field
                    label="Accession No"
                    v-model="accessionno"
                    required
                  ></v-text-field>
                </v-col>
  
                <v-file-input
                  label="Book Image"
                  filled
                  v-model="imageFile"
                  prepend-icon="mdi-camera"
                ></v-file-input>
              </v-row>
            </form>
          </div>
        </v-card-text>
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn color="blue darken-1" text @click="dialog = false">Close </v-btn>
          <v-btn color="blue darken-1" text @click="additem"> ADD </v-btn>
        </v-card-actions>
      </v-card>
    </div>
  </template>
  
  <script>
  import axios from "axios";
  export default {
    data() {
      return {
        snackAlert: false,
        dialog: false,
        title: "",
        category: "",
        author: "",
        publisher: "",
        accessionno: "",
        imageFile: null,
       
      };
    },
  
    methods: {
      async additem() {
        try {
          //   const newitem= {
          //       bookTitle:this.title,
          //       author:this.author,
          //       category:this.category,
          //       publisherName:this.publisher,
          //       accessionNo:this.accessionno,
          // },
          const newitem = [
            this.title,
            this.author,
            this.category,
            this.publisher,
            this.accessionno,
          ];
          const response = await axios.post( "${process.env.apiUrl}/admin/add_book",{ newitem }
          );
          console.log("item added", response.data);
          alert('Data added Sucessfully');
          this.$emit('item-added');
        } catch (error) {
          console.error("error adding data", error);  
        }
      },
    },
  };
  </script>