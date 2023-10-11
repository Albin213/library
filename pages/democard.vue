<template>
    <v-img :src="require('@/components/main.jpg')">
      <v-card class="transparent-card">
        <v-card-title>
          Title
        </v-card-title>
        <v-card-text>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit.
        </v-card-text>
        <v-card-actions>
          <v-btn @click="buttonClick">Click me</v-btn>
        </v-card-actions>
      </v-card>
    </v-img>
  </template>
  
  <style scoped>
  .transparent-card {
    background-color: rgba(255, 255, 255, 0.5); /* Adjust the alpha value to control transparency */
  }
  </style>
  
  <script>
  export default {
    methods: {
      buttonClick() {
        alert('Button clicked!');
        // Add your button click logic here
      },
    },
  };
  </script>
  