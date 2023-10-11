<!-- <template>
   
   <div>
    <navbar>

    
    <v-row>
    <h1>
  
        വിജ്ഞാന നഗരം - വായനശാല വാതിൽപ്പടിയിൽ
        </h1>
<v-spacer></v-spacer>
        <v-btn color="red lighten-1" > <v-icon>mdi-logout</v-icon>
              Logout
      </v-btn>
    </v-row>
</navbar>
    </div>
</template> -->



<template>
<header>
    <v-app>
      <v-navigation-drawer app center>
        <!-- Navigation drawer content goes here -->
      </v-navigation-drawer>
  
      <v-app-bar app center>
        <v-app-bar-nav-icon></v-app-bar-nav-icon>
        <v-spacer></v-spacer>
        <v-toolbar-title class="text-center">
          വിജ്ഞാന നഗരം - വായനശാല വാതിൽപ്പടിയിൽ
        </v-toolbar-title>
        <v-spacer></v-spacer>
        <v-btn color="red lighten-1">
          <v-icon>mdi-logout</v-icon>
          Logout
        </v-btn>
      </v-app-bar>
  


      <Dashboard />
      <!-- Main content of your page -->
      <v-main>
        <!-- Your page content goes here -->
      </v-main>
    </v-app>
  </header>
</template>


  

  