<script setup lang="ts">
import { ref } from "vue";
import QueueList from "@/components/QueueList.vue";

const auditionerData = ref([
  {
    fullName: "John Smith",
    pronouns: "he/him",
    age: 18,
    studentCell: "123-456-7890",
    studentEmail: "john.smith@example.com",
    parentName: "Jane Smith",
    parentCell: "987-654-3210",
    parentEmail: "jane.smith@example.com",
    status: "registered",
  },
  {
    fullName: "Emma Johnson",
    pronouns: "she/her",
    age: 16,
    studentCell: "111-222-3333",
    studentEmail: "emma.johnson@example.com",
    parentName: "David Johnson",
    parentCell: "444-555-6666",
    parentEmail: "david.johnson@example.com",
    status: "waiting",
  },
  {
    fullName: "Alex Brown",
    pronouns: "they/them",
    age: 17,
    studentCell: "555-666-7777",
    studentEmail: "alex.brown@example.com",
    parentName: "Sarah Brown",
    parentCell: "888-999-0000",
    parentEmail: "sarah.brown@example.com",
    status: "complete",
  },
  {
    fullName: "Olivia Davis",
    pronouns: "she/her",
    age: 15,
    studentCell: "999-888-7777",
    studentEmail: "olivia.davis@example.com",
    parentName: "Michael Davis",
    parentCell: "444-333-2222",
    parentEmail: "michael.davis@example.com",
    status: "registered",
  },
  {
    fullName: "William Johnson",
    pronouns: "he/him",
    age: 14,
    studentCell: "123-456-7890",
    studentEmail: "william.johnson@example.com",
    parentName: "Linda Johnson",
    parentCell: "987-654-3210",
    parentEmail: "linda.johnson@example.com",
    status: "waiting",
  },
  {
    fullName: "Sophia Anderson",
    pronouns: "she/her",
    age: 16,
    studentCell: "111-222-3333",
    studentEmail: "sophia.anderson@example.com",
    parentName: "Daniel Anderson",
    parentCell: "444-555-6666",
    parentEmail: "daniel.anderson@example.com",
    status: "complete",
  },
  {
    fullName: "Jacob Wilson",
    pronouns: "he/him",
    age: 17,
    studentCell: "555-666-7777",
    studentEmail: "jacob.wilson@example.com",
    parentName: "Emily Wilson",
    parentCell: "888-999-0000",
    parentEmail: "emily.wilson@example.com",
    status: "registered",
  },
  {
    fullName: "Mia Thompson",
    pronouns: "she/her",
    age: 15,
    studentCell: "999-888-7777",
    studentEmail: "mia.thompson@example.com",
    parentName: "Christopher Thompson",
    parentCell: "444-333-2222",
    parentEmail: "christopher.thompson@example.com",
    status: "waiting",
  },
  {
    fullName: "Ethan Martinez",
    pronouns: "he/him",
    age: 14,
    studentCell: "123-456-7890",
    studentEmail: "ethan.martinez@example.com",
    parentName: "Jennifer Martinez",
    parentCell: "987-654-3210",
    parentEmail: "jennifer.martinez@example.com",
    status: "complete",
  },
  {
    fullName: "John Smith",
    pronouns: "he/him",
    age: 18,
    studentCell: "123-456-7890",
    studentEmail: "john.smith@example.com",
    parentName: "Jane Smith",
    parentCell: "987-654-3210",
    parentEmail: "jane.smith@example.com",
    status: "registered",
  },
  {
    fullName: "Emma Johnson",
    pronouns: "she/her",
    age: 16,
    studentCell: "111-222-3333",
    studentEmail: "emma.johnson@example.com",
    parentName: "David Johnson",
    parentCell: "444-555-6666",
    parentEmail: "david.johnson@example.com",
    status: "waiting",
  },
  {
    fullName: "Alex Brown",
    pronouns: "they/them",
    age: 17,
    studentCell: "555-666-7777",
    studentEmail: "alex.brown@example.com",
    parentName: "Sarah Brown",
    parentCell: "888-999-0000",
    parentEmail: "sarah.brown@example.com",
    status: "complete",
  },
  {
    fullName: "Olivia Davis",
    pronouns: "she/her",
    age: 15,
    studentCell: "999-888-7777",
    studentEmail: "olivia.davis@example.com",
    parentName: "Michael Davis",
    parentCell: "444-333-2222",
    parentEmail: "michael.davis@example.com",
    status: "registered",
  },
  {
    fullName: "William Johnson",
    pronouns: "he/him",
    age: 14,
    studentCell: "123-456-7890",
    studentEmail: "william.johnson@example.com",
    parentName: "Linda Johnson",
    parentCell: "987-654-3210",
    parentEmail: "linda.johnson@example.com",
    status: "waiting",
  },
  {
    fullName: "Sophia Anderson",
    pronouns: "she/her",
    age: 16,
    studentCell: "111-222-3333",
    studentEmail: "sophia.anderson@example.com",
    parentName: "Daniel Anderson",
    parentCell: "444-555-6666",
    parentEmail: "daniel.anderson@example.com",
    status: "complete",
  },
  {
    fullName: "Jacob Wilson",
    pronouns: "he/him",
    age: 17,
    studentCell: "555-666-7777",
    studentEmail: "jacob.wilson@example.com",
    parentName: "Emily Wilson",
    parentCell: "888-999-0000",
    parentEmail: "emily.wilson@example.com",
    status: "registered",
  },
  {
    fullName: "Mia Thompson",
    pronouns: "she/her",
    age: 15,
    studentCell: "999-888-7777",
    studentEmail: "mia.thompson@example.com",
    parentName: "Christopher Thompson",
    parentCell: "444-333-2222",
    parentEmail: "christopher.thompson@example.com",
    status: "waiting",
  },
  {
    fullName: "Ethan Martinez",
    pronouns: "he/him",
    age: 14,
    studentCell: "123-456-7890",
    studentEmail: "ethan.martinez@example.com",
    parentName: "Jennifer Martinez",
    parentCell: "987-654-3210",
    parentEmail: "jennifer.martinez@example.com",
    status: "complete",
  },
  {
    fullName: "John Smith",
    pronouns: "he/him",
    age: 18,
    studentCell: "123-456-7890",
    studentEmail: "john.smith@example.com",
    parentName: "Jane Smith",
    parentCell: "987-654-3210",
    parentEmail: "jane.smith@example.com",
    status: "registered",
  },
  {
    fullName: "Emma Johnson",
    pronouns: "she/her",
    age: 16,
    studentCell: "111-222-3333",
    studentEmail: "emma.johnson@example.com",
    parentName: "David Johnson",
    parentCell: "444-555-6666",
    parentEmail: "david.johnson@example.com",
    status: "waiting",
  },
  {
    fullName: "Alex Brown",
    pronouns: "they/them",
    age: 17,
    studentCell: "555-666-7777",
    studentEmail: "alex.brown@example.com",
    parentName: "Sarah Brown",
    parentCell: "888-999-0000",
    parentEmail: "sarah.brown@example.com",
    status: "complete",
  },
  {
    fullName: "Olivia Davis",
    pronouns: "she/her",
    age: 15,
    studentCell: "999-888-7777",
    studentEmail: "olivia.davis@example.com",
    parentName: "Michael Davis",
    parentCell: "444-333-2222",
    parentEmail: "michael.davis@example.com",
    status: "registered",
  },
  {
    fullName: "William Johnson",
    pronouns: "he/him",
    age: 14,
    studentCell: "123-456-7890",
    studentEmail: "william.johnson@example.com",
    parentName: "Linda Johnson",
    parentCell: "987-654-3210",
    parentEmail: "linda.johnson@example.com",
    status: "waiting",
  },
  {
    fullName: "Sophia Anderson",
    pronouns: "she/her",
    age: 16,
    studentCell: "111-222-3333",
    studentEmail: "sophia.anderson@example.com",
    parentName: "Daniel Anderson",
    parentCell: "444-555-6666",
    parentEmail: "daniel.anderson@example.com",
    status: "complete",
  },
  {
    fullName: "Jacob Wilson",
    pronouns: "he/him",
    age: 17,
    studentCell: "555-666-7777",
    studentEmail: "jacob.wilson@example.com",
    parentName: "Emily Wilson",
    parentCell: "888-999-0000",
    parentEmail: "emily.wilson@example.com",
    status: "registered",
  },
  {
    fullName: "Mia Thompson",
    pronouns: "she/her",
    age: 15,
    studentCell: "999-888-7777",
    studentEmail: "mia.thompson@example.com",
    parentName: "Christopher Thompson",
    parentCell: "444-333-2222",
    parentEmail: "christopher.thompson@example.com",
    status: "waiting",
  },
  {
    fullName: "Ethan Martinez",
    pronouns: "he/him",
    age: 14,
    studentCell: "123-456-7890",
    studentEmail: "ethan.martinez@example.com",
    parentName: "Jennifer Martinez",
    parentCell: "987-654-3210",
    parentEmail: "jennifer.martinez@example.com",
    status: "complete",
  },
]);
auditionerData.value.forEach((aud) => {
  aud.id = Math.random();
});
function getProgressValue(): number {
  const complete = auditionerData.value.filter(
    (auditioner) => auditioner.status === "complete"
  ).length;
  return (100 * complete) / auditionerData.value.length;
}
</script>

<template>
  <v-container style="height: 100%">
    <v-row>
      <v-col>
        <div class="text-center text-h1">Musical Auditions</div>
        <div class="text-center text-subtitle-1">Theatre Company</div>
      </v-col>
    </v-row>
    <v-row>
      <v-col>
        <v-progress-linear
          :model-value="getProgressValue()"
          color="primary"
        ></v-progress-linear>
      </v-col>
    </v-row>
    <v-row class="queue-row">
      <v-col class="queue-col">
        <QueueList
          :auditioners="auditionerData"
          statusText="Registered"
          status="registered"
        />
      </v-col>
      <v-col class="queue-col">
        <QueueList
          :auditioners="auditionerData"
          statusText="Waiting Room"
          status="waiting"
        />
      </v-col>
      <v-col class="queue-col">
        <QueueList
          :auditioners="auditionerData"
          statusText="Complete"
          status="complete"
        />
      </v-col>
    </v-row>
  </v-container>
</template>

<style scoped>
.queue-row {
  height: 80%;
}

.queue-col {
  height: 90%;
}
</style>
