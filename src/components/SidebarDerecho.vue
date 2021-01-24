<template>
    <v-navigation-drawer permanent :right="true" app clipped width="400px">
        <template v-slot:prepend>
            <nav class="navegacion">
                <a href="#" class="navegacion__link navegacion__link--activo">Registro de actividad</a>
                <a href="#" class="navegacion__link">Perfil de Monitoreo</a>
            </nav>
            <v-divider></v-divider>
        </template>

        <v-card class="mx-auto mt-5 d-flex flex-no-wrap justify-space-between" max-width="90%">
            <div>
                <v-card-title v-text="'Infracción en los lineamientos'"></v-card-title>
                <v-card-subtitle v-text="'Área de Descargas - Cámara 2'"></v-card-subtitle>
                <v-card-subtitle v-text="'12:33 Hoy'"></v-card-subtitle>
            </div>

            <v-avatar class="ma-3" size="120" tile>
                <v-img src="../assets/no-video-background.png"></v-img>
            </v-avatar>
        </v-card>
        <template v-slot:append>
            <div class="text-center">
                <p>Actualizado por última vez - Hoy 12:24</p>
            </div>
        </template>

    </v-navigation-drawer>
</template>

<script>
    export default {
        name: 'SidebarDerecho',
        data() {
            return {
                items: [
                    { title: 'Home', icon: 'mdi-home-city' },
                    { title: 'My Account', icon: 'mdi-account' },
                    { title: 'Users', icon: 'mdi-account-group-outline' },
                ],
                lugares: ['Guadalajara Norte', 'Guadalajara Sur'],
            };
        },
    };
</script>

<style lang="scss" scoped>
    a {
        text-decoration: none;
    }
    .navegacion {
        background-color: white;
        display: flex;
        justify-content: center;
        gap: 10px;
    }

    .navegacion__link {
        font-weight: bold;
        color: rgb(185, 181, 181);
        padding: 10px;
        transition: 0.3s color ease-in;
        /* margin-right: 2rem; */
    }

    .navegacion__link--activo,
    .navegacion__link:hover {
        color: black;
        border-top: 3px solid #5386ff;
    }
</style>
