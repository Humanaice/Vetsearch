<template>
    <div style="background-color: #cdddfc;" class="h-auto">
        <v-container class="px-3 py-6">
            <v-row class="py-6 h-100 ">
                <v-col cols="12" md="7" class="d-flex flex-column align-center py-5 px-3 h-auto">
                    <v-row class="d-flex w-100">
                        <v-col cols="12" class="d-flex flex-column align-center text-center px-0"
                            style="height: fit-content;">
                            <span class="pt-2 pb-3 text-h5 title">Please select date and time</span>
                            <v-date-picker show-adjacent-months hide-header class="w-100 bg"
                                color="#f3f3f7"></v-date-picker>
                        </v-col>
                        <v-col cols="12" class="h-auto">
                            <v-btn-toggle rounded="0" v-model="toggle" color="primary" mandatory
                                class="d-flex flex-wrap h-auto pa-2 ">
                                <v-row class="d-flex justify-center align-center">
                                    <v-col cols="4" sm="3" v-for="(hour, index) in hours" class="py-1 px-1">
                                        <v-btn flat rounded="0" class="h-auto w-100 pa-6 btnHour" :value="hour">
                                            <span class="">{{ hour }}</span>
                                        </v-btn>
                                    </v-col>
                                </v-row>
                            </v-btn-toggle>
                        </v-col>
                    </v-row>


                    <!-- <v-row class="d-flex justify-center w-100 h-100">
                        <v-btn-toggle rounded="0" v-model="toggle" color="primary" mandatory
                            class="d-flex flex-wrap h-auto pa-2">
                            <v-row class="">
                                <v-col cols="4" sm="3" v-for="(hour, index) in hours" class="py-1 px-1">
                                    <v-btn flat rounded="0" class="h-auto w-100 pa-6 btnHour" :value="hour">
                                        <span class="">{{ hour }}</span>
                                    </v-btn>
                                </v-col>
                            </v-row>
                        </v-btn-toggle>
                    </v-row> -->
                    <!-- <div class="h-100 w-100">
                        A
                    </div> -->
                </v-col>
                <v-col cols="12" md="5" class="px-4 py-5 h-auto">
                    <div class="h-100 d-flex flex-column justify-space-between align-start bg">
                        <div cols="12" class="d-flex flex-column align-self-start px-0 py-2 w-100">
                            <span class="text-h5 pb-3 align-self-center title">Appointment informations</span>
                            <v-divider :thickness="1" class="border-opacity-100" color="#464373"></v-divider>
                            <div class="d-flex flex-column px-0 mx-0">
                                <div class="d-flex flex-column px-6 mx-6 mt-6">
                                    <span class="py-2">Appointment with Karen Miller</span>
                                    <span class="py-2">Willian Street, 7, Miami Orlando</span>
                                    <span class="py-2">12:20 until 13:00</span>
                                    <span class="pt-6">Which pet will go the veterinary?</span>
                                </div>
                                <div class="d-flex overflow-x-auto pt-4">
                                    <v-chip-group selected-class="text-primary" mandatory center-active show-arrows>
                                        <v-chip v-for="n in 40" variant="outlined" style="color: #3b73ce;">
                                            Adolfooooo
                                        </v-chip>
                                    </v-chip-group>
                                </div>
                            </div>
                        </div>

                        <div cols="12" class="d-flex flex-column w-100 px-4 pb-4 align-self-end">
                            <v-btn height="80" color="#ff6ea0" class="my-4">
                                <span class="whiteText text-h6 font-weight-bold">Make an account</span>
                            </v-btn>
                            <v-btn height="80" color="blue">
                                <span class="whiteText text-h6 font-weight-bold">Save in calendar</span>
                            </v-btn>
                        </div>
                    </div>
                </v-col>
            </v-row>

        </v-container>
    </div>
</template>

<script setup>
const toggle = ref(1100);
const hours = ref(["8:00", "9:00", "10:00", "11:00", "12:00", "13:00", "14:00", "15:00"])
</script>

<style lang="scss" scoped>
.title {
    color: #3b73ce;
    font-weight: bold;
}

.bg {
    background-color: #f3f3f7;
    border: 1px #464373 solid;
    color: #474276;
}

.btnHour {
    background-color: #f3f3f7;
    border: 1px #3b73ce solid;
}

.whiteText {
    color: #f3f3f7;
}
</style>