<template>
    <v-row class="d-flex justify-center">
        <v-col cols="10" sm="8" md="5">
            <v-row class="d-flex justify-start" style="background-color: white;border: 1px solid black;">
                <v-col cols="4" class="pa-0 d-flex justify-start"
                    style="background-color: white;border-right: 1px solid black;">
                    <v-img alt="John" src="/img/blankProfile.webp" aspect-ratio="14/9" cover></v-img>
                </v-col>
                <v-col cols="8" class="d-flex flex-column justify-space-between">
                    <div>
                        <span class="text-lg-h5 text-sm-h6 text-body-2">Return to the veterinarian</span><br>
                        <span class=" text-lg-body-1 text-caption">Karen Miller is waiting for the return of
                            Snow!</span>
                    </div>
                    <v-btn color="blue">Make an Appoinment</v-btn>
                </v-col>
            </v-row>
        </v-col>
    </v-row>
</template>

<script setup>

</script>

<style scoped></style>