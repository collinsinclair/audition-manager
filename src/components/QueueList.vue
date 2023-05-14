<script setup lang="ts">
import AuditionerCard from "@/components/AuditionerCard.vue";
</script>

<template>
  <v-container>
    <v-row>
      <v-col>
        <div class="text-center text-h2">Footloose the Musical</div>
        <div class="text-center text-h3">Front Range Theatre Company</div>
      </v-col>
    </v-row>
    <v-row>
      <v-col>
        <div class="text-center text-h4 mb-1">Registered</div>
        <v-card elevation="3" class="px-2 py-2">
          <v-text-field
            clearable
            label="Search"
            prepend-inner-icon="mdi-magnify"
            variant="outlined"
          ></v-text-field>
          <auditioner-card />
          <auditioner-card />
          <auditioner-card />
        </v-card>
      </v-col>
      <v-col>
        <h3 class="text-center text-h4 mb-1">Checked In</h3>
        <v-card elevation="3" class="px-2 py-2">
          <v-text-field
            clearable
            label="Search"
            prepend-inner-icon="mdi-magnify"
            variant="outlined"
          ></v-text-field>
          <auditioner-card />
          <auditioner-card />
          <auditioner-card />
        </v-card>
      </v-col>
      <v-col>
        <h3 class="text-center text-h4 mb-1">Complete</h3>
        <v-card elevation="3" class="px-2 py-2">
          <v-text-field
            clearable
            label="Search"
            prepend-inner-icon="mdi-magnify"
            variant="outlined"
          ></v-text-field>
          <auditioner-card />
          <auditioner-card />
          <auditioner-card />
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<style scoped></style>
