<template>
    <div style="background-color: #cdddfc;" class="h-auto">
        <v-container class="px-3 py-6">
            <v-row class="py-6">
                <v-col cols="12" md="7" class="d-flex flex-column align-center pa-5">
                    <span class="py-2 text-h5">Please select date and time</span>
                    <v-date-picker show-adjacent-months hide-header class="w-100 my-4"></v-date-picker>
                    <v-row class="d-flex justify-center">
                        <v-col cols="4" sm="3" v-for="n in 8">
                            <v-btn class="h-100 w-100 pa-4">11:00</v-btn>
                        </v-col>
                    </v-row>
                </v-col>
                <v-col cols="12" md="5" class="px-6 py-6 h-auto">
                    <div class="h-100 d-flex flex-column justify-space-between align-start"
                        style="background-color: white; border: 1px black solid;">
                        <div cols="12" class="d-flex flex-column align-self-start px-0 py-2 w-100">
                            <span class="text-h5 pb-3 align-self-center">Appointment informations</span>
                            <v-divider :thickness="1" class="border-opacity-100" color="black"></v-divider>
                            <div class="d-flex flex-column px-0 mx-0">
                                <div class="d-flex flex-column px-6 mx-6 mt-6">
                                    <span class="py-2">Appointment with Karen Miller</span>
                                    <span class="py-2">Willian Street, 7, Miami Orlando</span>
                                    <span class="py-2">12:20 until 13:00</span>
                                    <span class="pt-6">Which pet will go the veterinary?</span>
                                </div>
                                <div class="d-flex overflow-x-auto pt-4">
                                    <v-chip-group selected-class="text-primary" mandatory center-active show-arrows>
                                        <v-chip v-for="n in 40">
                                            Pet 1
                                        </v-chip>
                                    </v-chip-group>
                                </div>
                            </div>
                        </div>

                        <div cols="12" class="d-flex flex-column w-100 px-4 pb-4 align-self-end">
                            <v-btn height="80" color="red" class="my-4">Make an account</v-btn>
                            <v-btn height="80" color="blue">Save in calendar</v-btn>
                        </div>
                    </div>
                </v-col>
            </v-row>
        </v-container>
    </div>
</template>

<script setup>

</script>

<style lang="scss" scoped></style>