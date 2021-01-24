<template>
    <v-container>
        <v-row class="text-center justify-space-around">
            <v-col cols="12" class="text-left ml-0">
                <h1>
                    Centro de monitoreo
                </h1>
            </v-col>

            <v-col cols="12" class="mx-auto">
                <v-card max-width="100%">
                    <img src="../assets/no-video-background.png" alt="camara" width="100%" />
                    <div class="caja">
                        <div>
                            <v-icon large>mdi-chevron-left</v-icon>
                        </div>
                        <div>
                            <h3 class="mb-2">Cámara 2</h3>
                            <v-select filled v-model="lugares[0]" :items="lugares" dense></v-select>
                        </div>
                        <div>
                            <v-icon large>mdi-chevron-right</v-icon>
                        </div>
                    </div>
                    <v-divider></v-divider>
                    <div class="caja__botones">
                        <div class="caja__item">
                            <v-icon large>mdi-access-point</v-icon>
                            <p>En vivo</p>
                        </div>
                        <div class="caja__item">
                            <v-icon large>mdi-autorenew</v-icon>
                            <p>Historial</p>
                        </div>
                        <v-spacer></v-spacer>
                        <div class="caja__item">
                            <v-icon large>mdi-microphone</v-icon>
                            <p>Altavoz</p>
                        </div>
                        <div class="caja__item">
                            <v-icon large>mdi-car-brake-alert</v-icon>
                            <p>Alerta</p>
                        </div>
                    </div>
                </v-card>
            </v-col>

            <v-col cols="12" class="mx-auto">
                <v-card max-width="100%">
                    <h3 class="text-left ml-5 py-3">
                        Área de Carga
                    </h3>
                    <v-divider></v-divider>
                    <div class="galeria py-3">
                        <div v-for="(zona, i) in zonas" :key="i">
                            <img src="../assets/no-video-background.png" alt="camara" width="250px" />
                            <p>{{ zona }}</p>
                        </div>
                    </div>
                    <v-divider></v-divider>

                    <h3 class="text-left ml-5 py-3">
                        Zona de Empaquetado
                    </h3>
                    <v-divider></v-divider>
                    <div class="galeria py-3">
                        <div v-for="(zona, i) in zonas" :key="i">
                            <img src="../assets/no-video-background.png" alt="camara" width="250px" />
                            <p>{{ zona }}</p>
                        </div>
                    </div>

                     <v-divider></v-divider>

                    <h3 class="text-left ml-5 py-3">
                        Almacén Oeste
                    </h3>
                    <v-divider></v-divider>
                    <div class="galeria py-3">
                        <div v-for="(zona, i) in zonas2" :key="i">
                            <img src="../assets/no-video-background.png" alt="camara" width="250px" />
                            <p>{{ zona }}</p>
                        </div>
                    </div>
                </v-card>
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
    export default {
        name: 'MonitoreoPage',
        data() {
            return {
                lugares: ['Área de Carga'],
                zonas: [
                    'Pasillo Oeste',
                    'Operadores',
                    'Pasillo Sur',
                    'Verificador de Salida',
                    'Almacén Sur',
                    'Almacén Sur',
                ],
                zonas2: [
                    'Pasillo Oeste',
                    'Operadores',
                    'Pasillo Sur',
                ],
            };
        },
    };
</script>

<style lang="scss" scoped>
    .caja {
        display: flex;
        justify-content: space-around;
        padding: 10px;
        align-items: center;
        border-bottom: 1px solid rgb(185, 181, 181);
    }

    .caja__botones {
        display: flex;
        justify-content: space-evenly;
    }
    .caja__item {
        width: 100px;
        height: 100px;
        padding-top: 20px;
        border-left: 1px solid rgb(185, 181, 181);
        border-right: 1px solid rgb(185, 181, 181);
    }
    .caja__item p {
        margin: 0;
    }
    .galeria {
        display: grid;
        grid-template-columns: repeat(4, 1fr);
        column-gap: 5px;
        row-gap: 15px;
    }
</style>
