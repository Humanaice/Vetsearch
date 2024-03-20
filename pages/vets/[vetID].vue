<template>
    <div>
        <v-container fluid>
            <v-row class="d-flex justify-center">
                <v-col cols="12" class="d-flex justify-center">
                    <v-avatar size="150" style="border: 1px black solid;">
                        <v-img alt="John" src="/img/blankProfile.webp"></v-img>
                    </v-avatar>
                </v-col>
                <v-col class="d-flex justify-center">
                    <span class="text-h5 text-center font-weight-bold" style="color: #3b73ce;">Zé da Esquina</span>
                </v-col>
            </v-row>
        </v-container>
        <v-container fluid style="background: linear-gradient(white 50%,#cdddfc 50%);">
            <v-row class="d-flex justify-space-evenly">
                <v-col cols="10" sm="3" class="d-flex justify-center my-2"
                    style="background-color: #474276;color: white;">
                    <span class="d-flex justify-center">{{ stats.stars }}</span>
                </v-col>
                <v-col cols="10" sm="3" class="d-flex justify-center my-2"
                    style="background-color: #474276;color: white;">
                    <span class="d-flex justify-center">{{ stats.available }}</span>
                </v-col>
                <v-col cols="10" sm="3" class="d-flex justify-center my-2"
                    style="background-color: #474276;color: white;">
                    <span class="d-flex justify-center">{{ stats.city }}</span>
                </v-col>
            </v-row>
        </v-container>
        <v-container fluid style="background-color: #cdddfc;" class="h-auto">
            <v-col cols="12" class="d-flex justify-center">

            </v-col>
            <v-row class="d-flex justify-center pb-6">
                <v-col cols="10" sm="6" md="4" class="d-flex justify-center">
                    <v-btn color="blue" class="w-100 h-auto pa-5">
                        <span class="text-h5">Make an appointment</span>
                    </v-btn>
                </v-col>
                <v-col cols="12"></v-col>
                <v-col cols="10" sm="8" md="6">
                    <div class="d-flex flex-column justify-center pa-6"
                        style="background-color: white;border: black solid 1px;">
                        <span class="text-h5 text-center font-weight-bold pb-2" style="color: #3b73ce;">
                            More informations about veterinarian
                        </span>
                        <span class="font-weight-bold text-center pa-2">
                            Address: <span class="font-weight-light">{{ address }}</span>
                        </span>
                        <span class="font-weight-bold text-center pa-2">
                            Worktime: <span class="font-weight-light">{{ worktime }}</span>
                        </span>
                    </div>
                </v-col>
                <v-col cols="12" class="d-flex justify-center">
                    <span class="text-h5 text-center font-weight-bold" style="color: #3b73ce;">
                        Suggestions for you
                    </span>
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
    </div>
</template>

<script setup>
const stats = ref({ stars: "5 Stars", available: "Available", city: "Washinton DC" });
const address = ref("Richarlison Street, number 44, New York");
const worktime = ref("From Mondays to Thursdays, from 8:00 hours until 15:00 hours");
</script>

<style scoped></style>