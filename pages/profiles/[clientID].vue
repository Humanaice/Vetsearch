<template>
    <div>
        <v-container fluid>
            <v-row class="d-flex justify-center">
                <v-col cols="12"></v-col>
            </v-row>
        </v-container>
        <v-container fluid style="background: linear-gradient(white 50%,#cdddfc 50%);">
            <v-row class="d-flex justify-center">
                <v-col cols="12" class="d-flex justify-center">
                    <v-avatar size="150" style="border: 1px black solid;">
                        <v-img alt="John" src="/img/blankProfile.webp"></v-img>
                    </v-avatar>
                </v-col>
            </v-row>
        </v-container>
        <v-container fluid style="background-color: #cdddfc;" class="h-auto">
            <v-row class="d-flex justify-center pb-6">
                <v-col cols="12" class="d-flex justify-center">
                    <span class="text-h5 text-center font-weight-bold" style="color: #3b73ce;">Zé da Esquina</span>
                </v-col>
                <v-col cols="11" class="d-flex flex-column align-center justify-center">
                    <v-row class="d-flex justify-center pb-6 ">
                        <v-col v-for="pet in pets" class="py-0 px-1 d-flex justify-center align-center">
                            <PetInfo></PetInfo>
                        </v-col>
                    </v-row>
                    <v-btn color="blue" class="w-50" style="padding-top: 20px;padding-bottom: 35px;">
                        Add a new pet
                    </v-btn>
                </v-col>
                <v-col cols="12" class="d-flex justify-center">
                    <span class="text-h5 text-center font-weight-bold" style="color: #3b73ce;">
                        Upcoming appointments
                    </span>
                </v-col>
                <v-col cols="6">
                    <AptmtCard class="my-6"></AptmtCard>
                    <AptmtCard class="my-6"></AptmtCard>
                </v-col>
                <v-col cols="12" class="d-flex justify-center">
                    <span class="text-h5 text-center font-weight-bold" style="color: #3b73ce;">
                        Historic of appointments
                    </span>
                </v-col>
                <v-col cols="10">
                    <v-row class="d-flex justify-space-evenly">
                        <v-col cols="6">
                            <AptmtCard class="pr-2"></AptmtCard>
                        </v-col>
                        <v-col cols="6">
                            <AptmtCard class="pl-2"></AptmtCard>
                        </v-col>
                    </v-row>
                </v-col>
            </v-row>
        </v-container>
    </div>
</template>

<script setup>
import AptmtCard from './../../components/AptmtCard.vue';
import PetInfo from './../../components/PetInfo.vue';

const pets = ref([0, 1, 2, 3]);
</script>

<style lang="scss" scoped></style>