<template>
    <div>
      <Navbar />
      <div class="container">
        <Sidebar />
        <div class="content">
          <router-view />
        </div>
      </div>
    </div>
  </template>
  
  <script>
  import Navbar from '@/pages/navbar.vue';
  import Sidebar from '@/pages/sidebar.vue';
  
  export default {
    components: {
      Navbar,
      Sidebar,
    },
  };
  </script>
  
  <style>
  /* Add your styling here */
  </style>
  