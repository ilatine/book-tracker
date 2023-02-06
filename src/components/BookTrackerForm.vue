<script setup lang="ts">
import Card from "primevue/card";
import InputText from "primevue/inputtext";
import { ref } from "vue";

const name = ref("");
const author = ref("");
const totalPages = ref(0);
const started = ref("");
</script>

<template>
  <Card>
    <template #title> Book Tracker Form </template>
    <template #content>
      <div>
        <label>Book Name: </label
        ><InputText id="name" type="text" v-model="name" />
      </div>

      <div>
        <label>Author: </label
        ><InputText id="author" type="text" v-model="author" />
      </div>

      <div>
        <label>Total Pages: </label
        ><InputText id="totalPages" type="text" v-model="totalPages" />
      </div>

      <div>
        <label>Have you started?: </label
        ><InputText id="started" type="text" v-model="started" />
      </div>
    </template>
    <template #footer>
      <Button icon="pi pi-check" label="Save">Save</Button>
      <Button
        icon="pi pi-times"
        label="Cancel"
        class="p-button-secondary"
        style="margin-left: 0.5em"
        >Cancel</Button
      >
    </template>
  </Card>
</template>
