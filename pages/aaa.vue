<!-- <template>
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
  
   -->
  



   <!--  <template>
    <div>
      <Navbar />
      <div class="container"> 
        <Sidebar />
        
        <div class="content">
          <router-view /> -->
      

        <!-- <Dashboard /> <!- Add your Dashboard component here -->
        <!-- </div>
      </div>
    </div>
  </template> --> -
  
  <!-- <script>
  import Navbar from '@/pages/navbar.vue';
  import Sidebar from '@//pages/sidebar.vue';
  import Dashboard from '@/pages/dash.vue'; // Import your Dashboard component -->
  
  <!-- export default {
    components: {
      Navbar,
      Sidebar,
      Dashboard, // Include Dashboard in the components section
    },
  };
  </script>
  
  <style> -->
  <!-- /* Add your styling here */
  </style> --> 




  <template>
    <div>
      <Navbar />
      <Sidebar />
      <div class="container">
        <v-img :src="require('@/components/main.jpg')">
          <div>
            <v-row class="px-8 pt-8">
              <v-col lg="3" cols="3">
                <v-card class="mx-auto" max-width="400">
                  <v-card-text>
                    <v-img :src="require('@/components/Membership.jpg')"></v-img>
                  </v-card-text>
                  <v-card color="#33691E">
                    <router-link to="/membership" style="text-decoration:none">
                      <v-btn fab color="#8BC34A" elevation="0">
                        <v-icon class="mdi-account-plus">mdi-account-plus</v-icon>
                      </v-btn>
                    </router-link>
                    <v-list-item-title class="headline ml-1 mt-3 white--text">
                      Membership
                    </v-list-item-title>
                  </v-card>
                </v-card>
              </v-col>
              <v-col lg="3" cols="4">
                <v-card class="mx-auto" max-width="400">
                  <v-card-text>
                    <v-img :src="require('@/components/OrderPlaced.jpg')"></v-img>
                  </v-card-text>
                  <v-card color="#33691E">
                    <v-btn fab color="#8BC34A" elevation="0">
                      <v-icon color="my-icon-style-2">mdi-dolly</v-icon>
                    </v-btn>
                    <v-list-item-title class="headline ml-1 mt-3 white--text">
                      Order Placed
                    </v-list-item-title>
                  </v-card>
                </v-card>
              </v-col>
              <v-col lg="3" cols="4">
                <v-card class="mx-auto" max-width="400">
                  <v-card-text>
                    <v-img :src="require('@/components/BookRequest.jpg')"></v-img>
                  </v-card-text>
                  <v-card color="#33691E">
                    <v-btn fab color="#8BC34A" elevation="0">
                      <v-icon color="white">mdi-book</v-icon>
                    </v-btn>
                    <v-list-item-title class="headline ml-1 mt-3 white--text">
                      Book Requests
                    </v-list-item-title>
                  </v-card>
                </v-card>
              </v-col>
              <v-col lg="3" cols="4">
                <v-card class="mx-auto" max-width="400">
                  <v-card-text>
                    <v-img :src="require('@/components/BookReturn.jpg')"></v-img>
                  </v-card-text>
                  <v-card color="#33691E">
                    <v-btn fab color="#8BC34A" elevation="0">
                      <v-icon class="my-icon-style-2">mdi-refresh</v-icon>
                    </v-btn>
                    <v-list-item-title class="headline ml-1 mt-3 white--text">
                      Book Returns
                    </v-list-item-title>
                  </v-card>
                </v-card>
              </v-col>
            </v-row>
            <!-- More sections here -->
            <v-row>
              <v-col lg="3" cols="4">
                <v-card class="mx-auto" max-width="400">
                  <v-card-text>
                    <v-img :src="require('@/components/DeliveryPartner.jpg')"></v-img>
                  </v-card-text>
                  <v-card color="#33691E">
                    <v-btn fab color="#8BC34A" elevation="0">
                      <v-icon class="my-icon-style-2">mdi-truck-delivery</v-icon>
                    </v-btn>
                    <v-list-item-title class="headline ml-1 mt-3 white--text">
                      Delivery Partner
                    </v-list-item-title>
                  </v-card>
                </v-card>
              </v-col>
              <v-col lg="3" cols="4">
                <v-card class="mx-auto" max-width="400">
                  <v-card-text>
                    <v-img :src="require('@/components/booklist.jpg')"></v-img>
                  </v-card-text>
                  <v-card color="#33691E">
                    <router-link to="/bookmanagement" style="text-decoration:none">
                      <v-btn fab color="#8BC34A" elevation="0">
                        <v-icon class="my-icon-style-2">mdi-book</v-icon>
                      </v-btn>
                    </router-link>
                    <v-list-item-title class="headline ml-1 mt-3 white--text">
                      Book Management
                    </v-list-item-title>
                  </v-card>
                </v-card>
              </v-col>
            </v-row>
          </div>
        </v-img>
      </div>
    </div>
  </template>

<script>
import Navbar from '@/pages/navbar.vue';
import Sidebar from '@//pages/sidebar.vue';


 export default {
  components: {
    Navbar,
    Sidebar,
  
  },
};
</script>
  
  