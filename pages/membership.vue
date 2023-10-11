<!-- <template>
   
      <div class="pa-6">
  <v-card>
    <v-toolbar
      color="cyan"
      dark
      flat
    >
    <v-tabs
    v-model="memberStatus"
        centered
        slider-color="yellow"
        background-color="transparent"
        class="hidden-xs-only">

        <v-tab  class="mx-auto"
    color="secondary"
    width="200px">
          Membership Requests
        </v-tab>

        <v-tab>
          Members
        </v-tab>
        
        </v-tabs>
      </v-toolbar>
      
  <v-tabs-items v-model="memberStatus">
    </v-tabs-items>
    
   
  </v-card>
  
    </div>
    <script>
        export default {
            data(){
                return {
                    memberStatus:""
                }
            }
        }
          </script>
</template> -->



<template>
    <div class="pa-9">
      <v-card>
        <v-toolbar color="cyan" dark flat>
          <v-tabs
            v-model="memberStatus"
            centered
            slider-color="yellow"
            background-color="transparent"
            class="hidden-xs-only"
          >
            <v-tab color="secondary" width="300">
              Membership Requests
            </v-tab>
            <v-tab color="secondary" width="300">
              Members
            </v-tab>
          </v-tabs>
        </v-toolbar>
  
        <v-tabs-items v-model="memberStatus">
          <!-- Content for the "Membership Requests" tab -->
          <v-tab-item>
            <v-card>
              <v-card-text>
                <!-- Add your content for Membership Requests here -->
                <p>Membership Requests</p>
                <v-card>
      <v-card-title>
        Card Title
      </v-card-title>

      <v-card-text>
        <!-- Card content goes here -->
        This is some content for the card.
      </v-card-text>

      <!-- "View" button -->
      <v-card-actions>
        <v-btn color="primary">View</v-btn>
      </v-card-actions>
    </v-card>
              </v-card-text>
            </v-card>
          </v-tab-item>
  
          <!-- Content for the "Members" tab -->
          <v-tab-item>
            <v-card>
              <v-card-text>
                <!-- Add your content for Members here -->
                <p> Members</p>
                <v-card>
      <v-card-title>
        Card Title
      </v-card-title>

      <v-card-text>
        <!-- Card content goes here -->
        This is some content for the card.
      </v-card-text>

      <!-- "View" button -->
      <v-card-actions>
        <v-btn color="primary">View</v-btn>
      </v-card-actions>
    </v-card>
              </v-card-text>
            </v-card>
          </v-tab-item>
        </v-tabs-items>
      </v-card>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        memberStatus: "",
      };
    },
  };
</script>