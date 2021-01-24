<template>
    <v-app>
        <Sidebar />
        <Navbar />
        <v-main class="fondo">
            <monitoreo-page />
        </v-main>
        <sidebar-derecho />
    </v-app>
</template>

<script>
    import Navbar from './components/Navbar';
    import Sidebar from './components/Sidebar.vue';
    import SidebarDerecho from './components/SidebarDerecho.vue';
    import MonitoreoPage from './views/MonitoreoPage.vue';
    export default {
        name: 'App',
        components: {
            Navbar,
            Sidebar,
            SidebarDerecho,
            MonitoreoPage,
        },

        data: () => ({
            //
        }),
    };
</script>

<style lang="scss" scoped>
    .fondo {
        background-color: #f5f8ff;
    }
    .v-application {
      font-family: 'Barlow', sans-serif;
    }
</style>
