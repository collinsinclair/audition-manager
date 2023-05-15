<script setup lang="ts">
import { ref } from "vue";
import { auditionerProps } from "@/types";
let dialogOpen = ref(false);
const props = defineProps<{
  auditioner: auditionerProps;
}>();
function getNextAction(status: string): string | null {
  switch (status) {
    case "registered": {
      return "Check In";
    }
    case "waiting": {
      return "Mark Complete";
    }
    default: {
      return null;
    }
  }
}
function setNextAction(auditioner: auditionerProps): void {
  switch (auditioner.status) {
    case "registered": {
      auditioner.status = "waiting";
      break;
    }
    case "waiting": {
      auditioner.status = "complete";
    }
  }
  dialogOpen.value = false;
}

function getStatusColor(status: string): string {
  switch (status) {
    case "registered": {
      return "primary";
    }
    case "waiting": {
      return "warning";
    }
    case "complete": {
      return "success";
    }
    default: {
      return "grey";
    }
  }
}
</script>

<template>
  <v-hover>
    <template v-slot:default="{ isHovering, props }">
      <v-card
        elevation="2"
        class="px-1 py-1 mx-1 my-2"
        :color="isHovering ? 'grey-lighten-2' : ''"
        v-bind="props"
        @click="dialogOpen = true"
      >
        <v-card-title>
          {{ auditioner.fullName }} ({{ auditioner.age }})
          <v-badge
            dot
            style="float: right"
            :color="getStatusColor(auditioner.status)"
          ></v-badge>
        </v-card-title>
        <v-card-subtitle>{{ auditioner.pronouns }}</v-card-subtitle>
        <v-dialog v-model="dialogOpen" width="auto">
          <v-card>
            <v-card-title>
              {{ auditioner.fullName }} ({{ auditioner.age }})
              <v-icon
                icon="mdi-circle-medium"
                :color="getStatusColor(auditioner.status)"
                style="float: right"
              />
            </v-card-title>
            <v-card-subtitle>{{ auditioner.pronouns }}</v-card-subtitle>
            <v-card-text>
              <p class="font-weight-bold text-body-1">Student Contact Info</p>
              <p>Email: {{ auditioner.studentEmail }}</p>
              <p>Cell: {{ auditioner.studentCell }}</p>
              <v-divider></v-divider>
              <p class="font-weight-bold text-body-1">Parent Contact Info</p>
              <p>Name(s): {{ auditioner.parentName }}</p>
              <p>Email(s): {{ auditioner.parentEmail }}</p>
              <p>Cell(s): {{ auditioner.parentCell }}</p>
            </v-card-text>
            <v-card-actions v-if="getNextAction(auditioner.status)">
              <v-btn color="primary" @click="setNextAction(auditioner)">{{
                getNextAction(auditioner.status)
              }}</v-btn>
            </v-card-actions>
          </v-card>
        </v-dialog>
      </v-card>
    </template>
  </v-hover>
</template>

<style scoped></style>
