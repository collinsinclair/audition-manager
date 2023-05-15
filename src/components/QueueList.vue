<script setup lang="ts">
import AuditionerCard from "@/components/AuditionerCard.vue";
import { auditionerProps } from "@/types";
import { ref, computed } from "vue";

const props = defineProps<{
  auditioners: auditionerProps[];
  status: string;
  statusText: string;
}>();
let searchString = ref("");
const filteredAuditioners = computed(() => {
  return props.auditioners
    .filter((auditioner) => {
      if (auditioner.status === props.status) {
        if (searchString.value === "" || searchString.value === null) {
          return true;
        } else {
          return auditioner.fullName
            .toLowerCase()
            .includes(searchString.value.toLowerCase());
        }
      }
      return false;
    })
    .sort((a, b) => {
      return a.fullName.localeCompare(b.fullName);
    });
});
</script>

<template>
  <div class="text-center text-h5 mb-3">
    {{ statusText }} ({{ filteredAuditioners.length }})
  </div>
  <v-text-field
    clearable
    label="Search"
    prepend-inner-icon="mdi-magnify"
    variant="outlined"
    v-model="searchString"
    style="margin-bottom: -10px"
  ></v-text-field>
  <v-card elevation="3" class="cards px-2 py-2">
    <auditioner-card
      v-for="auditioner in filteredAuditioners"
      :auditioner="auditioner"
      :key="auditioner.id"
    />
  </v-card>
</template>

<style scoped>
.cards {
  max-height: 90%;
  overflow-y: auto;
}
</style>
