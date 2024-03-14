<template>
  <NuxtLayout>
    <v-container class="my-3">
      <v-row class="d-flex justify-center ma-3">
      </v-row>
    </v-container>
    <v-container fluid style="background: linear-gradient(white 50%,#cdddfc 50%);">
      <v-row class="d-flex justify-center">
        <v-col cols="6" class="d-flex justify-center" style="background-color: #3b73ce; color:white">
          <span class="text-h5">Find a veterinarian near you</span>
        </v-col>
      </v-row>
    </v-container>
    <v-container fluid style="background-color: #cdddfc;" class="h-100">
      <v-row class="d-flex justify-center">
        <v-col cols="12" class="d-flex justify-center">

        </v-col>
        <v-col cols="12" class="d-flex justify-center">
          <span>Suggestions for you</span>
        </v-col>
        <v-col cols="12" class="d-flex justify-center">
          <v-row class="d-flex justify-center">
            <DocNear class="pa-1"></DocNear>
            <DocNear class="pa-1"></DocNear>
            <DocNear class="pa-1"></DocNear>
          </v-row>
        </v-col>
        <v-col cols="12" class="d-flex justify-center">
          <span>Veterinarians near you</span>
        </v-col>
        <v-col cols="12" class="d-flex justify-center">

        </v-col>
      </v-row>
    </v-container>
  </NuxtLayout>
</template>

<script setup>
import DocNear from './components/DocNear.vue';
</script>

<style scoped>
.page {
  background-color: white;
}

.findVeterinarian {
  background-color: #474276;
  color: white;
  border-radius: 40px;
}
</style>