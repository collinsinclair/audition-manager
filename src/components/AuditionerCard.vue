<script setup lang="ts">
import { ref } from "vue";
let dialogOpen = ref(false);
</script>

<template>
  <v-hover>
    <template v-slot:default="{ isHovering, props }">
      <v-card
        class="px-1 py-1 mx-1 my-2"
        :color="isHovering ? 'grey-lighten-2' : ''"
        v-bind="props"
        @click="dialogOpen = true"
      >
        <v-card-title>Collin Sinclair</v-card-title>
        <v-card-subtitle>he/him/his</v-card-subtitle>
        <v-card-text><a href="tel:17203715712">(720) 371-5712</a></v-card-text>
        <v-dialog v-model="dialogOpen" width="auto">
          <v-card>
            <v-card-title>Collin Sinclair</v-card-title>
            <v-card-subtitle>he/him/his</v-card-subtitle>
            <v-card-text>Lorem ipsum el dolor sit amet.</v-card-text>
          </v-card>
        </v-dialog>
      </v-card>
    </template>
  </v-hover>
</template>

<style scoped></style>
