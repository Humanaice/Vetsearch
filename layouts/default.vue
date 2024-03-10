<template>
    <v-app>
        <v-container class="header" fluid>
            <v-row class="d-flex align-center">
                <v-col cols="1"></v-col>
                <v-col cols="1">
                    <span class="text-body-2 text-sm-body-1">BACK</span>
                </v-col>
                <v-col lg="3" md="3" sm="3"></v-col>
                <v-col class="d-flex justify-center pl-6" cols="2">
                    <span class="text-h6 text-sm-h4 font-weight-bold"><span
                            style="color: white;">VET</span>SEARCH</span>
                </v-col>
                <v-col class="d-none d-lg-flex justify-end pr-0 " cols="2" offset="">
                    <span class="">MY APPOINTMENTS</span>
                </v-col>
                <v-col class="d-none d-lg-flex justify-end" cols=2>
                    <!-- <span class="pl-15">MY APPOINTMENTS</span> -->
                    <span class="">MY ACCOUNT</span>
                </v-col>
                <v-col class="d-flex d-lg-none justify-end" cols="1" offset="3">
                    <v-app-bar-nav-icon class="" color="white" @click="DrawerChange()"></v-app-bar-nav-icon>
                </v-col>
                <v-navigation-drawer v-model="drawer" absolute location="right" color="#1a1939" disable-resize-watcher
                    disable-route-watcher :width="300">
                    <v-list-item prepend-avatar="./../blank-profile-picture-973460_960_720.webp"></v-list-item>
                    <v-list-item>
                        <div>
                            <v-expansion-panels>
                                <v-expansion-panel>
                                    <v-expansion-panel-title>
                                        <template v-slot:default="{ expanded }">
                                            <v-row no-gutters>
                                                <v-col class="d-flex justify-start" cols="4">
                                                    <v-avatar>
                                                        <v-img alt="John"
                                                            src="./../blank-profile-picture-973460_960_720.webp"></v-img></v-avatar>
                                                </v-col>
                                            </v-row>
                                        </template>
                                    </v-expansion-panel-title>
                                    <v-expansion-panel-text>
                                        <v-btn></v-btn>
                                    </v-expansion-panel-text>
                                </v-expansion-panel>
                            </v-expansion-panels>
                        </div>
                    </v-list-item>
                </v-navigation-drawer>
                <v-col cols=1></v-col>
            </v-row>
        </v-container>
        <div>
            <slot />
        </div>

        <v-footer app="true" class="pa-0">
            <v-container fluid class="footer">
                <v-row>
                    <v-col cols="1"></v-col>
                    <v-col cols="4">
                        <span class="text-sm-h6 text-body-1 font-weight-bold"><span
                                style="color: white;">VET</span>SEARCH</span>
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
                    <v-col cols="1"></v-col>
                    <v-col class="text-sm-h4 text-h6    ">
                        <i class="fa-brands fa-instagram icons pl-0"></i>
                        <i class="fa-brands fa-twitter icons"></i>
                        <i class="fab fa-facebook-f icons"></i>
                        <i class="fa-brands fa-youtube icons"></i>
                    </v-col>
                </v-row>
            </v-container>
        </v-footer>
    </v-app>
</template>

<script setup>
const drawerItems = ref(["MY ACCOUNT", "MY APPOINTMENTS"]);
var drawer = ref(false);

const DrawerChange = () => {
    console.log("Teste");
    drawer.value = !drawer.value;
}

const trip = reactive({ name: "", location: null, start: null, end: null })
const locations = ref(['Australia', 'Barbados', 'Chile', 'Denmark', 'Ecuador', 'France']);

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

.icons {
    color: white;
    /* font-size: 35px; */
    padding: 0px 15px;
}

.expansion {
    height: 50px;
}
</style>