<template>
  <div class="pa-6">
    <!-- Existing code here -->

    <!-- New Card with "View" button -->
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
