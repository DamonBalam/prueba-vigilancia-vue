<template>
    <v-navigation-drawer permanent :right="false" app>
        <template v-slot:prepend>
            <div class=" pa-4 pt-5">
                <v-img src="../assets/logo-grupo-morsa.png"></v-img>
            </div>
            <v-divider></v-divider>
            <div class="pa-3 pt-4">
                <v-select v-model="lugares[0]" :items="lugares" dense prepend-icon="mdi-fireplace-off" ></v-select>
            </div>
            <v-divider></v-divider>
        </template>

        <v-list dense>
            <v-subheader class="black--text">MONITOREO</v-subheader>
            <v-list-item v-for="item in items" :key="item.title">
                <v-list-item-icon>
                    <v-icon>{{ item.icon }}</v-icon>
                </v-list-item-icon>

                <v-list-item-content>
                    <v-list-item-title>{{ item.title }}</v-list-item-title>
                </v-list-item-content>
            </v-list-item>

            <v-subheader class="black--text">ADMINISTRACIÓN</v-subheader>
            <v-list-item v-for="item in items2" :key="item.title">
                <v-list-item-icon>
                    <v-icon>{{ item.icon }}</v-icon>
                </v-list-item-icon>

                <v-list-item-content>
                    <v-list-item-title>{{ item.title }}</v-list-item-title>
                </v-list-item-content>
            </v-list-item>
        </v-list>
    </v-navigation-drawer>
</template>

<script>
    export default {
        name: 'Sidebar',
        data() {
            return {
                items: [
                    { title: 'Centro de Monitoreo', icon: 'mdi-cctv' },
                    { title: 'Cámaras', icon: 'mdi-camera-metering-matrix' },
                    { title: 'Registro de Actividad', icon: 'mdi-camera-timer' },
                    { title: 'Analiticos', icon: 'mdi-finance' },
                ],
                items2: [
                    { title: 'Áreas', icon: 'mdi-semantic-web' },
                    { title: 'Dispositivos', icon: 'mdi-webcam' },
                    { title: 'CEDIS', icon: 'mdi-factory' },
                    { title: 'Usuarios', icon: 'mdi-account-supervisor' },
                ],
                lugares:[
                    'Guadalajara Norte',
                    'Guadalajara Sur',
                ]
            };
        },
    };
</script>

<style lang="scss" scoped></style>
