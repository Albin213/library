<!-- <template>
    <v-navigation-drawer permanent color="green" app>
      <v-list-item class="px-2 py-5">
        
        <v-img :src="require('@/components/image1.jpg')"></v-img>

      </v-list-item>
  
      <v-list dense>
        <v-list-item
          v-for="item in items"
          :key="item.text"
          link
        >
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title>{{ item.text }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </template>
  
  <script>
  
  export default {
    data: () => ({
      items: [
        { icon: 'mdi-view-dashboard', text: 'Dashboard'},
        { icon: 'mdi-account-plus', text:'Membership'  },
        {icon: 'mdi-dolly', text: 'Orders Placed'},
        { icon: 'mdi-book', text: 'Book Requests'},
      { icon: 'mdi-refresh', text: 'Books Return'},
      { icon: 'mdi-truck-delivery', text: 'Delivery Partner' },
    ],
    }),
    
  };
  
  
  </script> -->











  <template>
    <aside>
    <v-navigation-drawer  color="#33691E" app >
      <v-list-item class="px-2 py-5">


        <v-img :src="require('@/components/image1.jpg')"></v-img>



      </v-list-item>
  
      <v-list dense>
        <v-list-item
          v-for="item in items"
          :key="item.text"
          @click="navigateTo(item.route)" 
          link
        >
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>
          <v-list-item-content color="white">
            <v-list-item-title>{{ item.text }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </aside>
  </template>
  
  <script>
  export default {
    // layout:'sidebar',
    data: () => ({
      items: [
        { icon: 'mdi-view-dashboard', text: 'Dashboard', route: '/dash' },
        { icon: 'mdi-account-plus', text: 'Membership', route: '/membership' },
        { icon: 'mdi-dolly', text: 'Orders Placed', route: '/orders-placed' },
        { icon: 'mdi-book', text: 'Book Requests', route: '/book-requests' },
        { icon: 'mdi-refresh', text: 'Books Return', route: '/books-return' },
        { icon: 'mdi-truck-delivery', text: 'Delivery Partner', route: '/delivery-partner' },
        { icon: 'mdi-book', text: 'Book Management', route: '/bookmanagement' }


      ],
    }),
    methods: {
      navigateTo(route) {
        // Use Vue Router's programmatic navigation to navigate to the specified route
        this.$router.push(route);
      },
    },
  };
  </script>
  
  