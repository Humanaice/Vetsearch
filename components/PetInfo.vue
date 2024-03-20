<template>
    <div class="d-flex flex-column align-center">
        <div style="position:relative;top: 50px;">
            <v-avatar size="100" style="border: solid 1px black;">
                <v-img alt="John" src="/img/blankProfile.webp"></v-img>
            </v-avatar>
        </div>
        <div style="background-color: white;border: solid 1px black; padding: 60px 40px 20px 40px;">
            <v-row class="d-flex flex-column align-center">
                <v-col cols="12" class="d-flex justify-center pt-6">
                    <span>Deborah Ryan</span>
                </v-col>
                <v-col cols="12" class="d-flex justify-center pb-6 pt-0">
                    <span>0.4 km away from you</span>
                </v-col>
                <v-col cols="12" class="d-flex justify-center pt-1">
                    <v-btn>Change Info</v-btn>
                </v-col>
            </v-row>
        </div>

    </div>
</template>

<script setup>

</script>

<style lang="scss" scoped></style>