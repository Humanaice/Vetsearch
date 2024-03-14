<template>
  <NuxtLayout>
    <v-container class="my-6 d-flex justify-center">
      <div class="w-75">
        <v-row class="d-flex justify-center"
          style="background-color: #474276; border-radius: 40px;color: white; padding: 10px 20px;">
          <v-col lg="3" md="4" sm="6" cols="12" class="d-flex justify-md-center justify-sm-end justify-center pa-1">
            <span>I need a veterinarian in</span>
          </v-col>
          <v-col lg="3" md="4" sm="6" cols="12" class="d-flex justify-md-center justify-sm-start justify-center pa-1">
            <v-menu open-on-hover>
              <template v-slot:activator="{ props }">
                <v-btn v-bind="props" style="height: 25px;border-radius: 40px;">
                  <span v-if="Location != ''">{{ Location }}</span>
                  <span v-else>{{ LocationPreset }}</span>
                </v-btn>
              </template>

              <v-list>
                <v-list-item>

                </v-list-item>
              </v-list>
            </v-menu>
          </v-col>
          <v-col lg="1" md="1" sm="6" cols="12" class="d-flex justify-md-center justify-sm-end justify-center pa-1">
            <span>on the</span>
          </v-col>
          <v-col lg="2" md="3" sm="6" cols="12" class="d-flex justify-md-center justify-sm-start justify-center pa-1">
            <v-menu open-on-hover>

              <template v-slot:activator="{ props }">
                <v-btn v-bind="props" style="height: 25px;border-radius: 40px;">
                  <span v-if="DatePick != ''">{{ date.format(DatePick, "normalDateWithWeekday") }}</span>
                  <span v-else>{{ datePreset }}</span>
                </v-btn>
              </template>

              <v-list>
                <v-list-item>
                  <v-date-picker v-model="DatePick"></v-date-picker>
                </v-list-item>
              </v-list>
            </v-menu>
          </v-col>
        </v-row>
      </div>
    </v-container>
    <v-container fluid style="background: linear-gradient(white 50%,#cdddfc 50%);">
      <v-row class="d-flex justify-center">
        <v-col cols="6" class="d-flex justify-center" style="background-color: #3b73ce; color:white">
          <span class="text-h5 text-center">Find a veterinarian near you</span>
        </v-col>
      </v-row>
    </v-container>
    <v-container fluid style="background-color: #cdddfc;" class="h-auto">
      <v-row class="d-flex justify-center">
        <v-col cols="12" class="d-flex justify-center">
          <span class="text-h5 text-center" style="color: #3b73ce;">Suggestions for you</span>
        </v-col>
        <v-col cols="12" class="d-flex justify-center">
          <v-row class="d-flex justify-center">
            <DocNear class="pa-1"></DocNear>
            <DocNear class="pa-1"></DocNear>
            <DocNear class="pa-1"></DocNear>
          </v-row>
        </v-col>
        <v-col cols="12" class="d-flex justify-center">
          <span class="text-h5 text-center" style="color: #3b73ce;">Veterinarians near you</span>
        </v-col>
        <v-col cols="12" class="d-flex justify-center">
          <v-row class="d-flex justify-center">
            <VetNear class="pa-1"></VetNear>
            <VetNear class="pa-1"></VetNear>
            <VetNear class="pa-1"></VetNear>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </NuxtLayout>
</template>

<script setup>
import DocNear from './components/DocNear.vue';
import VetNear from './components/VetNear.vue';
import { useDate } from 'vuetify'

const LocationPreset = ref("city, district");
const Location = ref('');

const date = useDate()

const DatePreset = ref("date")
const DatePick = ref();




const formatted = date.format('Wed Mar 06 2024 00:00:00 GMT-0300 (Brasilia Standard Time)', 'keyboardDate')
console.log(formatted);
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