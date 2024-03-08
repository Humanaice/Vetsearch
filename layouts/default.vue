<template>
    <v-container class="header" fluid>
        <v-row class="d-flex align-center">
            <v-col offset="1" cols="1">
                <span class="">BACK</span>
            </v-col>
            <v-col lg="3" md="2" sm="1"></v-col>
            <v-col class="d-flex justify-center" cols="2">
                <span class="text-h4 font-weight-bold"><span style="color: white;">VET</span>SEARCH</span>
            </v-col>
            <v-col class="d-flex justify-end pr-0" cols="2" offset="">
                <span class="">MY APPOINTMENTS</span>
            </v-col>
            <v-col class="d-flex justify-end" cols=2>
                <!-- <span class="pl-15">MY APPOINTMENTS</span> -->
                <span class="">MY ACCOUNT</span>
            </v-col>
            <v-col cols=1></v-col>
        </v-row>
    </v-container>
    <div>
        <slot />
    </div>
    <v-container fluid class="footer">
        <v-row>
            <v-col cols="1"></v-col>
            <v-col cols="4">
                <span class="text-sm-h6 text-body-1 font-weight-bold"><span style="color: white;">VET</span>SEARCH</span>
            </v-col>
            <v-col cols="6">
                <div class="d-flex flex-column align-end">
                    <span class="text-body-2 text-sm-body-1 font-weight-bold">MY ACCOUNT</span>
                    <span class="text-body-2 text-sm-body-1 font-weight-bold">MY APPOINTMENTS</span>
                </div>
            </v-col>
            <v-col cols="1"></v-col>
        </v-row>
        <v-row>
            <v-icon icon="fa:fas fa-lock"></v-icon>
        </v-row>
    </v-container>
</template>

<script setup>

</script>

<style scoped>
    .header {
        background-color: #1a1939;
        color: #caddff;
        font-weight: 600;
    }
    .footer {
        background-color: #1a1939;
        color: #caddff;
    }
</style>