<template>
    <div>
        <v-row class="d-flex justify-center" style="background-color: white;border: 1px solid black;">
            <v-col v-if="firstTime" cols="4" class="pa-0 d-flex justify-start"
                style="background-color: white;border-right: 1px solid black;">
                <v-img alt="John" src="/img/blankProfile.webp" aspect-ratio="14/9" cover></v-img>
            </v-col>
            <v-col class="d-flex flex-column justify-space-between pa-6">
                <div class="d-flex flex-column">
                    <span class="text-lg-h5 text-sm-h6 text-body-1 pb-2" style="color: #4773c8;">
                        {{ title }}
                    </span>
                    <span class="text-caption text-sm-body-2 font-weight-bold">{{ context }}</span>

                </div>
                <div>
                    <div v-if="!firstTime" class="py-2">
                        <span class="text-caption">Address: {{ address }}</span><br>
                        <span class="text-caption">Time and date: {{ timeDate }}</span>
                    </div>
                    <v-btn color="blue" class="w-100" height="50">
                        <span class="text-body-2 text-sm-button">
                            {{ typeBtn }}
                        </span>
                    </v-btn>
                </div>

            </v-col>
        </v-row>
    </div>
</template>

<script setup>
const title = ref("Return to the veterinarian");
const context = ref("Karen Miller is waiting for the return of Snow!")
const firstTime = ref(false);
const address = ref("P. Sherman, 42, Wallaby Way, New York")
const timeDate = ref("11th November, 11:00 o’clock")
const typeBtn = ref("Make an Appoinment")
</script>

<style scoped></style>