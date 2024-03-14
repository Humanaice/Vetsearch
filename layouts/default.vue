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
                    <v-menu open-on-hover location="bottom center">
                        <template v-slot:activator="{ props }">
                            <v-btn v-bind="props" variant="text">
                                <span class="text-body-1">MY APPOINTMENTS</span>
                            </v-btn>
                        </template>
                        <v-list>
                            <v-list-item v-for="(Doctor, index) in appointments">
                                <v-row class="d-flex align-center">
                                    <v-col cols="3">
                                        <v-avatar size="50">
                                            <v-img :src="Doctor.image"></v-img>
                                        </v-avatar>
                                    </v-col>
                                    <v-col cols="5">
                                        <span class="overflow-x-auto">{{ Doctor.name }}</span>
                                    </v-col>
                                    <v-col cols="4">
                                        <v-btn>INFO</v-btn>
                                    </v-col>
                                </v-row>
                            </v-list-item>
                        </v-list>
                    </v-menu>
                </v-col>
                <v-col class="d-none d-lg-flex justify-end" cols=2>
                    <v-menu open-on-hover location="bottom center">

                        <template v-slot:activator="{ props }">
                            <v-btn v-bind="props" variant="text">
                                <span class="text-body-1">MY ACCOUNT</span>
                            </v-btn>
                        </template>

                        <v-list>
                            <v-list-item class="pb-4 pl-0">
                                <v-row class="pl-2">
                                    <v-col cols="4" class="px-6">
                                        <v-avatar size="80">
                                            <v-img alt="John" src="/img/blankProfile.webp"></v-img>
                                        </v-avatar>
                                    </v-col>
                                    <v-col cols="8" class="pl-2">
                                        <div class="d-flex flex-column">
                                            <span class="text-h5">Nome da Pessoa</span>
                                            <span class="text-caption">email@gmail.com</span>
                                            <span class="text-caption ">Logout</span>
                                        </div>
                                    </v-col>
                                </v-row>
                            </v-list-item>
                            <v-divider></v-divider>
                            <v-list-item v-for="(pet, index) in animal">
                                <v-row class="d-flex align-center">
                                    <v-col cols="3">
                                        <v-avatar size="50">
                                            <v-img :src="pet.image"></v-img>
                                        </v-avatar>
                                    </v-col>
                                    <v-col cols="5">
                                        <div class="overflow-x-auto" style="width: 100px;">
                                            <span>
                                                {{ pet.name }}
                                            </span>
                                        </div>

                                    </v-col>
                                    <v-col cols="4">
                                        <v-btn>INFO</v-btn>
                                    </v-col>
                                </v-row>
                            </v-list-item>
                        </v-list>
                    </v-menu>
                    <!-- <span class="">MY ACCOUNT</span> -->
                </v-col>
                <v-col class="d-flex d-lg-none justify-end" cols="1" offset="3">
                    <v-app-bar-nav-icon class="" color="white" @click="DrawerChange()"></v-app-bar-nav-icon>
                </v-col>
                <v-navigation-drawer v-model="drawer" :location="drawerLocation" absolute color="#1a1939"
                    disable-resize-watcher disable-route-watcher :width="drawerSize">
                    <v-list-item>
                        <v-row>
                            <v-col cols="2">
                                <v-app-bar-nav-icon class="" color="white" @click="DrawerChange()"></v-app-bar-nav-icon>
                            </v-col>
                            <v-col cols="8" class="d-flex align-center text-center justify-center">
                                <span class="text-h4 text-sm-h4 font-weight-bold" style="color: #caddff;"><span
                                        style="color: white;">VET</span>SEARCH</span>
                            </v-col>
                            <v-col cols="2"></v-col>
                        </v-row>
                    </v-list-item>
                    <v-list-item class="pb-4">
                        <v-row class="pl-2">
                            <v-col cols="4">
                                <v-avatar size="80">
                                    <v-img alt="John" src="/img/blankProfile.webp"></v-img>
                                </v-avatar>
                            </v-col>
                            <v-col cols="8" class="pl-0">
                                <div class="d-flex flex-column">
                                    <span class="text-h5">Nome da Pessoa</span>
                                    <span class="text-caption">email@gmail.com</span>
                                    <span class="text-caption ">Logout</span>
                                </div>
                            </v-col>
                        </v-row>
                    </v-list-item>
                    <v-divider class="pa-2"></v-divider>
                    <v-list-item>
                        <div>
                            <v-expansion-panels>
                                <v-expansion-panel>
                                    <v-expansion-panel-title>

                                        <template v-slot:default="{ expanded }">
                                            <v-row no-gutters>
                                                <v-col class="d-flex justify-start" cols="4">
                                                    <i class="fa-solid fa-dog px-1"></i>
                                                    <i class="fa-solid fa-cat px-1"></i>
                                                    <i class="fa-solid fa-paw px-1"></i>
                                                </v-col>
                                                <v-col cols="6">PETS</v-col>
                                            </v-row>
                                        </template>
                                    </v-expansion-panel-title>
                                    <v-expansion-panel-text>
                                        <v-row v-for="(pet, index) in animal" class="d-flex align-center">
                                            <v-col cols="3">
                                                <v-avatar size="50">
                                                    <v-img :src="pet.image"></v-img>
                                                </v-avatar>
                                            </v-col>
                                            <v-col cols="5">
                                                <div class="overflow-x-auto" style="width: 100px;">
                                                    <span>
                                                        {{ pet.name }}
                                                    </span>
                                                </div>

                                            </v-col>
                                            <v-col cols="4">
                                                <v-btn>INFO</v-btn>
                                            </v-col>
                                        </v-row>
                                    </v-expansion-panel-text>
                                </v-expansion-panel>
                            </v-expansion-panels>
                        </div>
                    </v-list-item>
                    <v-list-item>
                        <div>
                            <v-expansion-panels>
                                <v-expansion-panel>
                                    <v-expansion-panel-title>

                                        <template v-slot:default="{ expanded }">
                                            <v-row no-gutters>
                                                <v-col class="d-flex justify-start" cols="4">
                                                    <i class="fa-solid fa-dog px-1"></i>
                                                    <i class="fa-solid fa-cat px-1"></i>
                                                    <i class="fa-solid fa-paw px-1"></i>
                                                </v-col>
                                                <v-col cols="6">VETERINARIAN</v-col>
                                            </v-row>
                                        </template>
                                    </v-expansion-panel-title>
                                    <v-expansion-panel-text>
                                        <v-row v-for="(Doctor, index) in appointments" class="d-flex align-center">
                                            <v-col cols="3">
                                                <v-avatar size="50">
                                                    <v-img :src="Doctor.image"></v-img>
                                                </v-avatar>
                                            </v-col>
                                            <v-col cols="5">
                                                <span class="overflow-x-auto">{{ Doctor.name }}</span>
                                            </v-col>
                                            <v-col cols="4">
                                                <v-btn>INFO</v-btn>
                                            </v-col>
                                        </v-row>
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

        <div app class="pa-0">
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
                    <v-col class="text-sm-h4 text-h6">
                        <i class="fa-brands fa-instagram icons pl-0"></i>
                        <i class="fa-brands fa-twitter icons"></i>
                        <i class="fab fa-facebook-f icons"></i>
                        <i class="fa-brands fa-youtube icons"></i>
                    </v-col>
                </v-row>
            </v-container>
        </div>
    </v-app>
</template>

<script setup>
import { onMounted, watch } from 'vue'
import { useDisplay } from 'vuetify'

const { xs } = useDisplay()
const drawerLocation = ref("right");
const drawerSize = ref(360);

const drawerItems = ref(["MY ACCOUNT", "MY APPOINTMENTS"]);
var drawer = ref(false);

const DrawerChange = () => {
    console.log("Teste");
    console.log(xs.value)
    drawer.value = !drawer.value;
    drawerLocation.value = xs.value ? "bottom" : "right";
    drawerSize.value = xs.value ? 500 : 360;
}


const animal = ref({
    dog: { name: "DanteAAAAAAAAAAAAAAAAAAAAAAAAAAAA", image: '/img/blankProfile.webp', pg: "" },
    cat: { name: "Luz", image: '/img/blankProfile.webp', pg: "" },
    bunny: { name: "Cueio", image: '/img/blankProfile.webp', pg: "" },
})

const appointments = ref({
    DraAddams: { name: "Dra.Addams", image: '/img/blankProfile.webp', pg: "" },
    DrMatheus: { name: "Dr.Matheus", image: '/img/blankProfile.webp', pg: "" },
    DraDebora: { name: "Dra.Debora", image: '/img/blankProfile.webp', pg: "" },
})

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
</style>