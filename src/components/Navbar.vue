<template>
    <v-app-bar app color="#fff" elevation="1" height="65"  :clipped-left="false" :clipped-right="true">
        <!-- <div class="d-flex align-center">
            <v-img src="../assets/logo-grupo-morsa.png"></v-img>
        </div> -->
        <!-- <v-divider vertical ></v-divider> -->
        <v-spacer></v-spacer>
        <v-btn text fab>
            <v-icon large color="#C4CDD5">mdi-account-circle</v-icon>
        </v-btn>
    </v-app-bar>
</template>

<script>
    export default {
        name: 'Navbar',
    };
</script>

<style lang="scss" scoped>


</style>
